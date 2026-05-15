---
description: 置換変数は、リクエスト URLから画像カタログに保存された合成テンプレートに値を転送するために使用されます。 変数を使用して、複雑なリクエスト内の異なる場所に同じ値を伝えることもできます。
solution: Experience Manager
title: 置換変数
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
TQID: 'https://experienceleague.adobe.com/ZjLvcRUPDVBv8QsWoQGz2j6X0sjxnUL-MTTJNyDDRUs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 740
ht-degree: 0%

---

# 置換変数{#substitution-variables}

置換変数は、リクエスト URLから画像カタログに保存された合成テンプレートに値を転送するために使用されます。 変数を使用して、複雑なリクエスト内の異なる場所に同じ値を伝えることもできます。

` $ *`var`*= *`値`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>変数名。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">値</span> </span> </p> </td> 
  <td class="stentry"> <p>変数を設定する値（文字列）。 </p> </td> 
 </tr> 
</table>

変数の定義と参照は、リクエストのクエリ部分、`catalog::Modifier`および`catalog::PostModifier`で発生する可能性があります。

変数は、他のIS コマンドと同様に上記のように定義されます。先頭の&#39;$&#39;は、コマンドを変数定義として識別します。 変数は、参照する前に定義する必要があります。

変数名&#x200B;*`var`*&#x200B;は大文字と小文字を区別せず、ASCII文字、数字、「 – 」、「_」、「。」の組み合わせで構成される可能性があります。

>[!NOTE]
>
>*`value`*&#x200B;は、安全なHTTP送信のためにシングルパス URL エンコードする必要があります。 *`value`*&#x200B;がHTTP経由で再送信される場合は、ダブルエンコーディングが必要です。 これは、*`value`*&#x200B;がネストされた外部リクエストまたはSVG `<image>`要素のhref属性に置き換えられる場合に発生します。

変数参照は、先頭と末尾の&#39;$&#39; （$*var*$）で区切られた変数名で構成されます。 参照は、任意のIS コマンドの値部分（つまり、コマンド名の後の&#39;=&#39;とその後の&#39;&amp;&#39;またはリクエストの最後の間）のどこでも発生する可能性があります。 カスタム変数は、`layer=`および`effect=` コマンドに適用できません。 同じコマンド値で複数の変数を使用できます。 サーバーは、` $ *`var`*$`の各出現を&#x200B;*`value`*&#x200B;に置き換えます。

変数参照はネストできません。 *`value`*&#x200B;内の` $ *`var`*$`の出現箇所は置換されません。

例えば、リクエストフラグメントは次のようになります。

`$var2=apple&$var1=my$var2$tree&text=$var1$`

次の項目に解決します。

`text=my$var2$tree`

>[!NOTE]
>
>「$」は予約済みの文字ではありません。それ以外の場合は、リクエストで発生する可能性があります。 例えば、`src=my$image$file.tif`は有効なコマンドです（`my$image$file.tif`という名前のカタログエントリまたは画像ファイルが存在すると仮定します）。一方、`wid=$number$`はそうではありません。`wid`には数値引数が必要です。

## ネストされたリクエストでの変数処理 {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$`参照は、ネストされた画像サービングまたは画像レンダリング要求の中の中括弧の中のどこでも発生する可能性があります。これには、パスをクエリから分離する「?」の左側も含まれます。 サーバーは、ネストされたリクエストをさらに解析して処理する前に、これらの参照を値（URLまたはメイン画像カタログの`catalog::Modifier`から）に置き換えます。

さらに、URLまたは`catalog::Modifier`からのすべての` $ *`var`*=`定義は、ネストされたすべての画像サービングおよび画像レンダリング要求に転送されます。 これにより、ネスト レベルに関係なく、すべての変数定義がすべてのテンプレートで使用できるようになります。

ネスト レベルに関係なく、ネストされた画像レンダリングまたは画像サービングのリクエスト、または関連する`catalog::Modifier`文字列のどこでも置換される変数値には、シングルパス HTTP エンコーディングのみを適用する必要があります。

## 埋め込まれた外部リクエストでの変数処理 {#section-314e39a9aefb46faa737fd137897d1b0}

埋め込まれた外部リクエストの中かっこ内のどこかで発生する` $ *`var`*$`参照は、一致する変数定義値で置き換えられます。 これにより、埋め込まれた外部リクエストを画像カタログ内のテンプレートに配置できます。

サーバーが最終的な外部URLの送信を試みる前に再エンコーディングが適用されないため、通常、外部リクエストに置換される変数値はダブルエンコードする必要があります。

## SVG ファイルでの変数処理 {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$`参照は、属性値および`<text>`文字列のSVG ファイルで発生する可能性があります。 Image Servingは、SVG ファイルが指定されているリクエストネスティングレベルで既知の一致する` $ *`var`*=`定義でこれらを置き換えます。

>[!NOTE]
>
>`href`属性値に代入する変数値は、二重URL エンコードにする必要があります。その他はすべて単一エンコードする必要があります。

## 定義済みのパス変数 {#section-930d0dd12e8f49499becc9fe8df24092}

リクエストパスで指定された&#x200B;*`object`*&#x200B;は、事前定義済みの変数`*`$オブジェクト `*`に割り当てられます。 &#39;` $ *` オブジェクト `*$`&#39;は、リクエスト内の任意の場所、リクエストによって参照されるテンプレート、またはそのようなオブジェクトが許可されるネスト/埋め込みリクエスト（値`src=`および`mask=`、ネスト/埋め込みリクエストのパスなど）に配置できます。

例えば、次のリクエストでは、パスで指定された画像を、ネストされたリクエストのレイヤーのソースとして再利用します。

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

これは

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

`*`$object`*`の定義は、目的の値で` $ *`object`*=`を明示的に指定することで上書きできます。

定義済みのパス変数は、一般的に`template=`と組み合わせて使用されます。

## 初期設定 {#section-b02483d15529444586a2e9504805b155}

なし 定義された変数のみがサーバーで置換されます（ただし、常に置換される事前定義済みのパス変数$objectは除きます）。 `*`var`*`が既存の変数定義と一致しない場合、` $ *`var`*$`の出現箇所はリテラルのままになります。

## 例 {#section-fba9393df6984247b7e30b3f93992e86}

[&#x200B; テンプレート &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の「サンプル A」を参照してください。

## 関連項目 {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[&#x200B; テンプレート &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)、[&#x200B; テンプレート=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
