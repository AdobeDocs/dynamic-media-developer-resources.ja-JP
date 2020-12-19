---
description: 置換変数は、要求URLの値を、イメージカタログに保存されているテンプレートを合成するために使用します。 変数は、複雑なリクエストの様々な場所に同じ値を伝えるためにも使用できます。
seo-description: 置換変数は、要求URLの値を、イメージカタログに保存されているテンプレートを合成するために使用します。 変数は、複雑なリクエストの様々な場所に同じ値を伝えるためにも使用できます。
seo-title: 代替変数
solution: Experience Manager
title: 代替変数
topic: Scene7 Image Serving - Image Rendering API
uuid: e369f2c3-8d89-4169-8869-f1d7ab89aab9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---


# 置換変数{#substitution-variables}

置換変数は、要求URLの値を、イメージカタログに保存されているテンプレートを合成するために使用します。 変数は、複雑なリクエストの様々な場所に同じ値を伝えるためにも使用できます。

` $ *``*= *`varvalue`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>変数名。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>変数を設定する値（文字列）。 </p> </td> 
 </tr> 
</table>

変数の定義と参照は、リクエストのクエリ部分、`catalog::Modifier`、および`catalog::PostModifier`で発生する場合があります。

変数は、他のISコマンドと同様、上記のように定義されます。先頭の「$」は、コマンドが変数定義であることを示します。 変数は、参照前に定義する必要があります。

*`var`*&#x200B;変数名は大文字と小文字が区別されません。また、ASCII文字、数字、「 — 」、「_」、「。」の組み合わせで構成することもできます。

>[!NOTE]
>
>*`value`* は、安全なHTTP送信を目的として、1パスでURLエンコードする必要があります。*`value`*&#x200B;がHTTP経由で再送信される場合は、重複エンコーディングが必要です。 これは、*`value`*&#x200B;がネストされた外部リクエストに置換された場合、またはSVG `<image>`要素のhref属性に置換された場合の例です。

変数参照は、変数名の先頭と末尾にある「$」($*var*$)で区切られます。 参照は、ISコマンドの値部分のどこでも使用できます（例えば、コマンド名の後の「=」と、後続の「&amp;」または要求の終わりの間）。 カスタム変数は、`layer=`および`effect=`コマンドに適用できません。 同じコマンド値で複数の変数を使用できます。 サーバは、` $ *`var`*$`を&#x200B;*`value`*&#x200B;で置き換えます。

変数参照は入れ子にできません。 *`value`*&#x200B;内の` $ *`var`*$`は置換されません。

例えば、リクエストフラグメントは次のようになります。

`$var2=apple&$var1=my$var2$tree&text=$var1$`

解決されます。

`text=my$var2$tree`

>[!NOTE]
>
>「$」は予約文字ではありません。リクエスト内では、それ以外の場合に発生する可能性があります。 例えば、`src=my$image$file.tif`は有効なコマンドです（`my$image$file.tif`という名前のカタログエントリまたは画像ファイルが存在する場合）。`wid=$number$`は、`wid`には数値引数が必要なので、これは存在しません。

## 入れ子にされた要求{#section-26d63adc446c4fa0808e11e8082abdfa}での変数処理

` $ *``*$` varreferencesは、入れ子になった画像サービングまたは画像レンダリング要求の中括弧内（「?」の左を含む）で中括弧内の任意の場所に含めることができます。をクエリから切り離す。 サーバは、これらの参照を（メイン画像カタログのURLまたは`catalog::Modifier`からの）値で置き換えてから、ネストされた要求をさらに解析して処理します。

さらに、urlまたは`catalog::Modifier`のすべての` $ *`var`*=`定義が、ネストされたすべての画像サービングおよび画像レンダリング要求に転送されます。 これにより、ネストレベルに関係なく、すべてのテンプレートですべての変数定義を使用できます。

ネストのレベルに関係なく、1パスのHTTPエンコーディングのみを、ネストされた画像レンダリングまたは画像サービング要求の任意の場所に置換される変数値、または関連する`catalog::Modifier`文字列に適用する必要があります。

## 埋め込まれた外部要求で変数処理{#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`埋め込まれた外部要求の中括弧内の任意の場所で発生する`*$` varreferenceは、一致する変数定義値に置き換えられます。これにより、埋め込まれた外部要求を画像カタログのテンプレートに配置できます。

外部要求で置き換えられる変数値は、通常、重複エンコードする必要があります。これは、サーバーが最終的な外部URLの送信を試行する前に再エンコードが適用されないためです。

## SVGファイルでの変数処理{#section-a8359f9909764142b6a18ae778dca913}

` $ *`SVGファイル内の属性値と`*$` 文字列内に `<text>` varreferencesが存在する場合があります。画像サービングは、SVGファイルが指定されている要求のネストレベルにある、一致する` $ *`var`*=`定義に置き換えます。

>[!NOTE]
>
>`href`属性値に置き換えられる変数値は、重複URLでエンコードする必要があります。その他のすべては単独でエンコードする必要があります。

## 事前定義されたパス変数{#section-930d0dd12e8f49499becc9fe8df24092}

要求パスで指定された&#x200B;*`object`*&#x200B;は、事前定義の変数` *`$object`*`に割り当てられます。 &#39; ` $ *`object`*$`&#39;は、リクエスト内、リクエストが参照するテンプレート内、または`src=`と`mask=`の値、入れ子/埋め込みリクエストのパスなど、そのようなオブジェクトが許可される入れ子/埋め込みリクエスト内の任意の場所に配置できます。

例えば、次のリクエストは、パスで指定された画像をネストされたリクエスト内のレイヤーのソースとして再利用します。

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

これは、

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

` *`$object`*`の定義は、` $ *`object`*=`を目的の値で明示的に指定することで上書きできます。

定義済みのパス変数は、通常`template=`と組み合わせて使用されます。

## 初期設定 {#section-b02483d15529444586a2e9504805b155}

なし. サーバは、定義済みの変数のみを置き換えます（事前定義のパス変数$objectを除き、常に置き換えられます）。 ` $ *`var`*$`は、` *`var`*`が既存の変数定義と一致しない場合、リテラルのままです。

## 例 {#section-fba9393df6984247b7e30b3f93992e86}

[テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の「例A」を参照してください。

## 関連項目 {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)、 [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
