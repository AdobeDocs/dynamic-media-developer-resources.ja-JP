---
description: 代替変数は、リクエスト URL からイメージカタログに保存されているテンプレートを合成するために値を転送するために使用されます。 変数は、複雑なリクエストの様々な場所に同じ値を伝えるためにも使用できます。
solution: Experience Manager
title: 代替変数
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# 代替変数{#substitution-variables}

代替変数は、リクエスト URL からイメージカタログに保存されているテンプレートを合成するために値を転送するために使用されます。 変数は、複雑なリクエストの様々な場所に同じ値を伝えるためにも使用できます。

` $ *`var`*= *`値`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>変数名。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 値 </span> </span> </p> </td> 
  <td class="stentry"> <p>変数を設定する値（文字列）です。 </p> </td> 
 </tr> 
</table>

変数の定義と参照は、リクエストのクエリ部分で、 `catalog::Modifier`、および `catalog::PostModifier`.

変数は、他の IS コマンドと同様に上記のように定義されます。先頭の「$」は、コマンドを変数定義として識別します。 変数は、参照前に定義する必要があります。

変数名 *`var`* は大文字と小文字を区別せず、ASCII 文字、数字、「 — 」、「_」、「。」の組み合わせで構成することもできます。

>[!NOTE]
>
>*`value`* は、安全な HTTP 送信を目的として、1 パスで URL エンコードする必要があります。 次の場合は二重エンコードが必要です。 *`value`* は、HTTP を介して再送信されます。 これは *`value`* は、ネストされた外部リクエストまたはSVGの href 属性に置き換えられます。 `<image>` 要素を選択します。

変数参照は、変数名の先頭と末尾に「$」 ($*var*$) です。 参照は、任意の IS コマンドの値部分内の任意の場所に配置できます（つまり、コマンド名の後の「=」と、後続の「&amp;」またはリクエストの最後の間）。 カスタム変数は `layer=` および `effect=` コマンド。 同じコマンド値で複数の変数を使用できます。 サーバーは、 ` $ *`var`*$` 次を使用 *`value`*.

変数参照はネストできません。 次のいずれかの ` $ *`var`*$` 範囲 *`value`* は置換されません。

例えば、要求フラグメントは次のようになります。

`$var2=apple&$var1=my$var2$tree&text=$var1$`

解決先：

`text=my$var2$tree`

>[!NOTE]
>
>「$」は予約文字ではありません。リクエスト内で別の文字が使用される場合があります。 例： `src=my$image$file.tif` は有効なコマンドです ( カタログエントリまたは画像ファイルの名前が `my$image$file.tif` が存在する )、 `wid=$number$` がではないのは、 `wid` には数値引数が必要です。

## ネストされたリクエストでの変数処理 {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$` 参照は、「?」の左側を含め、ネストされた画像サービングまたは画像レンダリング要求の中括弧内の任意の場所で発生する可能性があります。 クエリからパスを分離する。 サーバーは、これらの参照を (URL または `catalog::Modifier` （メイン画像カタログの）) ネストされたリクエストをさらに解析および処理する前に呼び出します。

さらに、 ` $ *`var`*=` url からの定義または `catalog::Modifier` は、ネストされたすべての画像サービングおよび画像レンダリング要求に転送されます。 これにより、ネストのレベルに関係なく、すべての変数定義をすべてのテンプレートで使用できます。

ネストのレベルに関係なく、ネストされた画像レンダリング要求、画像サービング要求の任意の場所で置き換えられる変数の値、または関連する値には、1 パスの HTTP エンコードのみを適用する必要があります `catalog::Modifier` 文字列。

## 埋め込まれた外部リクエストでの変数処理 {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`var`*$` 埋め込まれた外部リクエストの中括弧内で発生する参照は、一致する変数定義値に置き換えられます。 これにより、埋め込まれた外部リクエストを画像カタログのテンプレートに配置できます。

外部要求で置き換えられる変数の値は、通常、二重エンコードする必要があります。サーバーが最終的な外部 URL を送信しようとする前に再エンコードが適用されないからです。

## 変数の処理 (SVGファイル ) {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$` 参照は、属性値のSVGファイル内および `<text>` 文字列。 画像サービングは、これらを一致する ` $ *`var`*=` SVG・ファイルが指定されているリクエスト・ネスト・レベルでの定義。

>[!NOTE]
>
>任意の変数値で、 `href` 属性値は、二重の URL エンコードが必要です。それ以外の値はすべて単独でエンコードする必要があります。

## 事前定義済みのパス変数 {#section-930d0dd12e8f49499becc9fe8df24092}

The *`object`* リクエストパスで指定された値は、事前定義済みの変数に割り当てられます `*`$object`*`. &#39; ` $ *`object`*$`&#39;は、リクエストの任意の場所、リクエストで参照されるテンプレート内、またはこのようなオブジェクトが許可されるネストされた/埋め込みリクエスト内（の値を含む）に配置できます。 `src=` および `mask=`、およびネストされた/埋め込み要求のパス。

例えば、次のリクエストでは、パスで指定された画像をネストされたリクエストのレイヤーのソースとして再利用します。

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

これは、

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

の定義 `*`$object`*` を明示的に指定することで上書きできます。 ` $ *`object`*=` を適切な値に設定します。

事前定義されたパス変数は、 `template=`.

## 初期設定 {#section-b02483d15529444586a2e9504805b155}

なし. 定義された変数だけがサーバに置き換えられます（定義済みのパス変数$object は常に置き換えられます）。 次のいずれかの ` $ *`var`*$` ～の場合は文字通りである `*`var`*`は既存の変数定義と一致しません。

## 例 {#section-fba9393df6984247b7e30b3f93992e86}

詳しくは、 [テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 関連項目 {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
