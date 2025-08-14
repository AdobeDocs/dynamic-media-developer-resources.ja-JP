---
description: 代替変数は、リクエスト URL の値を、画像カタログに格納された合成テンプレートに転送するために使用されます。 また、変数を使用して、同じ値を複雑なリクエスト内の異なる場所に伝えることもできます。
solution: Experience Manager
title: 代替変数
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 0%

---

# 代替変数{#substitution-variables}

代替変数は、リクエスト URL の値を、画像カタログに格納された合成テンプレートに転送するために使用されます。 また、変数を使用して、同じ値を複雑なリクエスト内の異なる場所に伝えることもできます。

` $ *`var`*= *`value`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>変数名。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 値 </span> </span> </p> </td> 
  <td class="stentry"> <p>変数を設定する値（文字列）。 </p> </td> 
 </tr> 
</table>

変数の定義と参照は、リクエストのクエリ部分、`catalog::Modifier`、`catalog::PostModifier` で発生する場合があります。

変数は、他の IS コマンドと同様に、上記のように定義されます。先頭の「$」は、コマンドを変数定義として識別します。 変数は、参照する前に定義する必要があります。

変数名 *`var`* では大文字と小文字が区別されず、ASCII 文字、数字、「–」、「_」、「。」の任意の組み合わせで構成される可能性があります。

>[!NOTE]
>
>安全な HTTP 送信を行うには、*`value`* をシングルパス URL エンコードする必要があります。 HTTP 経由で再送信する場合 *`value`* ダブルエンコーディングが必要です。 これは、*`value`* がネストされた外部リクエストまたはSVG `<image>` 要素の href 属性に置き換えられる場合です。

変数参照は、先頭と末尾の「$」（$*var*$）で区切られた変数名で構成されています。 参照は、任意の IS コマンドの値部分（つまり、コマンド名の後の「=」と、後続の「&amp;」またはリクエストの末尾）のどこでも発生する可能性があります。 カスタム変数は、`layer=` および `effect=` コマンドには適用できません。 同じコマンド値に複数の変数を含めることができます。 サーバーは ` $ *`var`*$` を *`value`* で置き換えます。

変数参照はネストできません。 ` $ *` 内で `*$`var *`value`* を使用しても、代用されません。

例えば、リクエストフラグメントは次のようになります。

`$var2=apple&$var1=my$var2$tree&text=$var1$`

解決先：

`text=my$var2$tree`

>[!NOTE]
>
>「$」は予約文字ではありません。リクエスト内で別の文字が使用されている可能性があります。 例えば、`src=my$image$file.tif` は有効なコマンドですが（`my$image$file.tif` という名前のカタログエントリまたは画像ファイルが存在すると仮定）、`wid=$number$` は有効ではありません。`wid` には数値の引数が必要だからです。

## ネストされたリクエストでの変数の処理 {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$` 参照は、「?」の左側を含め、ネストされた画像サービングまたは画像レンダリングリクエストの中括弧内のどこでも発生する可能性があります。 パスとクエリを分離しています。 サーバーは、ネストされたリクエストをさらに解析して処理する前に、これらの参照を（url またはメイン画像カタログの `catalog::Modifier` から）値に置き換えます。

さらに、URL または ` $ *` からのすべての `*=`var`catalog::Modifier` 定義は、ネストされたすべての画像サービングリクエストと画像レンダリングリクエストに転送されます。 これにより、ネストレベルに関係なく、すべての変数定義をすべてのテンプレートで使用できるようになります。

ネストのレベルに関係なく、ネストされた画像レンダリングまたは画像サービングリクエストまたはそれらに関連する `catalog::Modifier` 文字列の任意の場所で置き換える変数値には、シングルパス HTTP エンコーディングのみを適用します。

## 埋め込まれた外部リクエストの変数処理 {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`var`*$` 埋め込まれた外部リクエストの中括弧のどこかに存在する参照は、対応する変数定義値に置き換えられます。 これにより、埋め込まれた外部リクエストを画像カタログのテンプレートに配置できます。

通常、外部リクエストに置き換える変数値はダブルエンコードする必要があります。サーバーが最終的な外部 URL を送信しようとする前に、再エンコードが適用されないからです。

## SVG ファイルでの変数の処理 {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$` 参照は、SVG ファイルの属性値および `<text>` の文字列で発生する場合があります。 画像サービングでは、SVG ファイルが指定されているリクエストネストレベルで認識される、一致する ` $ *`var`*=` 定義でこれらを置き換えます。

>[!NOTE]
>
>`href` 属性値に置き換える変数値は、ダブル URL エンコードする必要があります。その他はすべて単独でエンコードする必要があります。

## 事前定義済みのパス変数 {#section-930d0dd12e8f49499becc9fe8df24092}

リクエストパスで指定された *`object`* は、事前定義済みの変数 `*`$object`*` に割り当てられます。 「` $ *`object`*$`」は、リクエスト内、リクエストによって参照されるテンプレート内、またはネストされた/埋め込みリクエスト内の任意の場所に配置できます。これらのリクエストでは、`src=` と `mask=` の値、ネストされた/埋め込みリクエストのパスなど、これらのオブジェクトが許可されます。

例えば、次のリクエストは、パスで指定された画像をネストされたリクエストのレイヤーのソースとして再利用します。

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

これは次と同等です

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

`*`$object`*` の定義は、` $ *`object`*=` を目的の値に明示的に指定することで上書きできます。

事前定義済みのパス変数は、`template=` と組み合わせて一般的に使用されます。

## 初期設定 {#section-b02483d15529444586a2e9504805b155}

なし。 定義済みの変数のみがサーバーによって置換されます（常に置換される事前定義済みのパス変数$object を除く）。 ` $ *`var`*$` を既存の変数定義と一致させることができない場合、`*`var`*` の出現箇所はすべてリテラルのままになります。

## 例 {#section-fba9393df6984247b7e30b3f93992e86}

[ テンプレート ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) の「例 A」を参照してください。

## 関連項目 {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[ テンプレート ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
