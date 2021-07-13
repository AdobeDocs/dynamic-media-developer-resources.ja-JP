---
description: 代替変数は、要求URLからイメージカタログに格納された合成テンプレートに値を転送するために使用されます。 変数は、複雑なリクエストの様々な場所に同じ値を伝えるためにも使用できます。
solution: Experience Manager
title: 代替変数
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# 代替変数{#substitution-variables}

代替変数は、要求URLからイメージカタログに格納された合成テンプレートに値を転送するために使用されます。 変数は、複雑なリクエストの様々な場所に同じ値を伝えるためにも使用できます。

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

変数の定義と参照は、リクエストのクエリ部分（`catalog::Modifier`内、および`catalog::PostModifier`内）で発生する場合があります。

変数は、他のISコマンドと同様に、上記のように定義されます。先頭の「$」は、コマンドを変数定義として識別します。 変数は、参照前に定義する必要があります。

変数名&#x200B;*`var`*&#x200B;は大文字と小文字を区別しません。また、ASCII文字、数字、「 — 」、「_」、「。」の組み合わせで構成することもできます。

>[!NOTE]
>
>*`value`* は、安全なHTTP送信を実現するために、1パスでURLエンコードする必要があります。*`value`*&#x200B;がHTTP経由で再送信される場合は、二重エンコーディングが必要です。 これは、*`value`*&#x200B;がネストされた外部リクエストに、またはSVG `<image>`要素のhref属性に置き換えられる場合に発生します。

変数参照は、先頭と末尾に「$」($*var*$)を区切った変数名で構成されます。 参照は、ISコマンドの値部分の任意の場所で発生する場合があります（例：コマンド名の後の「=」と、後続の「&amp;」またはリクエストの終わりの間）。 カスタム変数は、`layer=`および`effect=`コマンドには適用できません。 同じコマンド値で複数の変数を使用できます。 サーバは、` $ *`var`*$`を&#x200B;*`value`*&#x200B;に置き換えます。

変数参照はネストできません。 *`value`*&#x200B;内の` $ *`var`*$`は置換されません。

例えば、要求フラグメントは次のようになります。

`$var2=apple&$var1=my$var2$tree&text=$var1$`

解決：

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39;は予約文字ではありません。リクエスト内で別の場合に発生する可能性があります。 例えば、`src=my$image$file.tif`は有効なコマンドです（`my$image$file.tif`という名前のカタログエントリまたは画像ファイルが存在する場合）が、`wid=$number$`は有効ではありません。`wid`には数値引数が必要です。

## ネストされたリクエストでの変数処理 {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *``*$` varreferencesは、ネストされた画像サービング要求または画像レンダリング要求の中括弧内の任意の場所で、「?」の左側を含めて発生する可能性があります。クエリからパスを分離する。 サーバーは、ネストされた要求をさらに解析および処理する前に、これらの参照を(メイン画像カタログのURLまたは`catalog::Modifier`の値で置き換えます。

さらに、URLまたは`catalog::Modifier`からの` $ *`var`*=`定義がすべて、ネストされたすべての画像サービング要求および画像レンダリング要求に転送されます。 これにより、ネストレベルに関係なく、すべてのテンプレートですべての変数定義を使用できます。

ネストのレベルに関係なく、単一パスのHTTPエンコーディングのみを、ネストされた画像レンダリング要求または画像サービング要求の任意の場所、または関連する`catalog::Modifier`文字列に置き換える変数値に適用する必要があります。

## 埋め込み外部リクエストでの変数処理 {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`埋め込み外部リクエストの中括弧内の任意の場所にある`*$` varreferencesは、一致する変数定義値に置き換えられます。これにより、埋め込まれた外部リクエストを画像カタログのテンプレートに配置できます。

変数値で外部要求に置き換える場合は、通常、二重エンコードする必要があります。これは、サーバーが最終的な外部URLを送信しようとする前に再エンコードが適用されないからです。

## SVGファイルでの変数処理 {#section-a8359f9909764142b6a18ae778dca913}

` $ *``*$` varreferencesは、SVGファイルの属性値と文字列で発生する場合があ `<text>` ります。画像サービングは、SVGファイルが指定されている要求のネストレベルで認識されている、一致する` $ *`var`*=`定義をこれに置き換えます。

>[!NOTE]
>
>`href`属性値に置き換える変数値は、二重にURLエンコードする必要があります。それ以外の場合は、単独でエンコードする必要があります。

## 事前定義済みのパス変数 {#section-930d0dd12e8f49499becc9fe8df24092}

リクエストパスで指定された&#x200B;*`object`*&#x200B;は、事前定義された変数`*`$object`*`に割り当てられます。 &#39; ` $ *`object`*$`&#39;は、リクエスト、リクエストで参照されるテンプレート、または`src=`と`mask=`の値、ネスト/埋め込みリクエストのパスなど、このようなオブジェクトが許可されるネスト/埋め込みリクエストの任意の場所に配置できます。

例えば、次のリクエストでは、パスで指定された画像をネストされたリクエストのレイヤーのソースとして再利用します。

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

これは、

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

`*`$object`*`の定義は、必要な値で` $ *`object`*=`を明示的に指定することで上書きできます。

事前に定義されたパス変数は、`template=`と組み合わせて使用するのが一般的です。

## 初期設定 {#section-b02483d15529444586a2e9504805b155}

なし. 定義された変数のみがサーバに置き換えられます（事前に定義されたパス変数$objectは常に置き換えられます）。 ` $ *`var`*$`の出現箇所は、`*`var`*`と既存の変数定義とが一致しない場合、リテラルのままです。

## 例 {#section-fba9393df6984247b7e30b3f93992e86}

[テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の「例A」を参照してください。

## 関連項目 {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)、 [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
