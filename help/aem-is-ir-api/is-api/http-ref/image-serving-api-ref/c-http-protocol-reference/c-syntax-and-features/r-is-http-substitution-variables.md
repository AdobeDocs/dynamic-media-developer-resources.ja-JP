---
description: 置換変数は、要求URLの値を、画像カタログに保存されている合成テンプレートに転送するために使用されます。 変数を使用して、複雑なリクエストの異なる場所に同じ値を伝えることもできます。
seo-description: 置換変数は、要求URLの値を、画像カタログに保存されている合成テンプレートに転送するために使用されます。 変数を使用して、複雑なリクエストの異なる場所に同じ値を伝えることもできます。
seo-title: 代替変数
solution: Experience Manager
title: 代替変数
topic: Scene7 Image Serving - Image Rendering API
uuid: e369f2c3-8d89-4169-8869-f1d7ab89aab9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 代替変数{#substitution-variables}

置換変数は、要求URLの値を、画像カタログに保存されている合成テンプレートに転送するために使用されます。 変数を使用して、複雑なリクエストの異なる場所に同じ値を伝えることもできます。

` $ *``*= *`varvalue`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span></span> </p> </td> 
  <td class="stentry"> <p>変数名。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 価 </span> 値 </span> </p> </td> 
  <td class="stentry"> <p>変数を設定する値（文字列）。 </p> </td> 
 </tr> 
</table>

変数の定義と参照は、リクエストのクエリー部分、およびで使用 `catalog::Modifier`できます `catalog::PostModifier`。

変数は、他のISコマンドと同様に、上記のように定義されます。先頭の「$」は、コマンドを変数定義として識別します。 変数は、参照する前に定義する必要があります。

変数名では大 *`var`* 文字と小文字が区別されません。また、ASCII文字、数字、「 — 」、「_」、「。」の任意の組み合わせで構成できます。

>[!NOTE]
>
>*`value`* は、安全なHTTP送信を目的として、シングルパスURLエンコードする必要があります。 HTTP経由で再送信する場合は、二重エ *`value`* ンコーディングが必要です。 これは、がネストされた外 *`value`* 部リクエストまたはSVG要素のhref属性に置き換えられた場合の例 `<image>` です。

変数参照は、変数名の先頭と末尾の「$」($*var*$)で区切られます。 参照は、ISコマンドの値部分の任意の場所（例えば、コマンド名の後の「=」と、その後の「&amp;」またはリクエストの最後の間）で発生します。 カスタム変数は、およびコマンドに適用 `layer=` できま `effect=` せん。 同じコマンド値で複数の変数を使用できます。 サーバは、 ` $ *`varの各値を`*$`*`value`*.

変数参照はネストできません。 内の ` $ *`varは`*$` 、置換 *`value`* されません。

例えば、リクエストフラグメントは次のようになります。

`$var2=apple&$var1=my$var2$tree&text=$var1$`

解決される：

`text=my$var2$tree`

>[!NOTE]
>
>「$」は予約文字ではありません。リクエスト内で発生する可能性があります。 例えば、は有 `src=my$image$file.tif` 効なコマンドです（カタログエントリまたは画像ファイルが存在すると仮定します）。 `my$image$file.tif` は、数 `wid=$number$` 値引数が必要なた `wid` め、存在しません。

## ネストされたリクエストでの変数処理 {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var参照`*$` は、ネストされた画像サービングまたは画像レンダリング要求の中括弧内（「?」の左を含む）の任意の場所で使用できます。 パスをクエリーから分離する。 サーバーは、ネストされた要求をさらに解析して処理する前に、これらの参照を値(URLまたはメ `catalog::Modifier` イン画像カタログの値)で置き換えます。

さらに、URLまたは ` $ *`VAR定義は`*=` 、ネストされたすべての画像サービ `catalog::Modifier` ングおよび画像レンダリング要求に転送されます。 これにより、ネストレベルに関係なく、すべてのテンプレートですべての変数定義を使用できます。

ネストレベルに関係なく、単一パスのHTTPエンコーディングのみを変数値に適用する必要があります。変数値は、ネストされた画像レンダリング、画像サービング要求、または関連する文字列の任意の場所で置き換えら `catalog::Modifier` れます。

## 埋め込まれた外部要求での変数処理 {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`埋め込み`*$` 外部リクエストの中括弧内の任意の場所で発生するvar参照は、一致する変数定義値で置き換えられます。 これにより、埋め込まれた外部リクエストを画像カタログのテンプレートに配置できます。

外部要求に置き換えられる変数値は、通常、二重エンコードする必要があります。これは、サーバーが最終的な外部URLの送信を試行する前に再エンコードが適用されないためです。

## SVGファイルでの変数処理 {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var参照は`*$` 、SVGファイルの属性値と文字列で発生する場合があ `<text>` ります。 画像サービングは、SVGファイルが指定され ` $ *`ている要求の入れ子レベルで`*=` 、一致するvar定義をこれに置き換えます。

>[!NOTE]
>
>属性値に置き換える変数値は、二重にURLエ `href` ンコードする必要があります。その他のすべては単独でエンコードする必要があります。

## 事前定義されたパス変数 {#section-930d0dd12e8f49499becc9fe8df24092}

リクエスト *`object`* パスで指定した値は、事前定義された変数$objectに割り当て ` *`られます`*`。 &#39; ` $ *`object`*$`&#39;は、リクエスト、リクエストで参照されるテンプレート、またはネスト/埋め込みされたリクエスト内の任意の場所に配置できます。この場合、およびの値、入れ子/埋め込みリクエストのパスなど、このオブジェクトが許可さ `src=``mask=`れます。

例えば、次のリクエストでは、パスで指定された画像をネストされたリクエストのレイヤーのソースとして再利用します。

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

これは、

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

$objectの定義は、目的の値で ` *`object`*` を明示的に指定することで ` $ *`上書きでき`*=` ます。

定義済みのパス変数は、一般に、と組み合わせて使用されま `template=`す。

## 初期設定 {#section-b02483d15529444586a2e9504805b155}

なし. 定義された変数のみがサーバによって置き換えられます（事前定義されたパス変数$objectを除き、常に置き換えられます）。 varが既存の変数 ` $ *`定義と一致`*$` しない ` *``*`場合、varの出現はリテラルのままです。

## 例 {#section-fba9393df6984247b7e30b3f93992e86}

テンプレートの「例A」を参照して [ください](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 関連項目 {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
