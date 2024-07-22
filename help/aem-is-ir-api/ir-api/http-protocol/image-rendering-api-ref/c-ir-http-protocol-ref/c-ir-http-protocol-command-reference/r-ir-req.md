---
title: 要
description: リクエストタイプ。 リクエストされたデータのタイプを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b4a78a1-4f03-47ce-b523-10975e83f0ea
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 3%

---

# 要{#req}

リクエストタイプ。 リクエストされたデータのタイプを指定します。

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> debug </span> </p> </td> 
  <td class="stentry"> <p>コマンドをデバッグモードで実行します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> contents </span> </p> </td> 
  <td class="stentry"> <p>ビネット内のオブジェクトに関する情報を返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img </span> </p> </td> 
  <td class="stentry"> <p>コマンドを実行し、レンダリング イメージを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> imageprops </span> </p> </td> 
  <td class="stentry"> <p>指定したビネットのプロパティを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> map </span> </p> </td> 
  <td class="stentry"> <p>ビネットに埋め込まれた画像マップデータを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> object </span> </p> </td> 
  <td class="stentry"> <p>コマンドを実行し、マスクされたレンダリング イメージを現在のオブジェクト選択に戻します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> props </span> </p> </td> 
  <td class="stentry"> <p>コマンドを実行して、返信画像のプロパティを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> userdata </span> </p> </td> 
  <td class="stentry"> <p>Vignette::UserData </span> の内容 <span class="codeph"> 返します。 </p> </td> 
 </tr> 
</table>

詳細な説明に特に記載がない限り、サーバーは MIME タイプ &lt;text/plain> のテキスト応答を返します。

`debug`

指定したコマンドを実行し、レンダリング イメージを返します。 エラーが発生した場合は、エラー画像の代わりにエラーとデバッグの情報が返されます（`attribute::ErrorImagePath`）。

`contents`

選択されたオブジェクト属性を含む、ビネット内のオブジェクト階層の XML 表現を返します。 リクエスト内のその他のコマンドは無視されます。

`img`

指定したコマンドを実行し、レンダリング イメージを返します。 返信データの形式と応答のタイプは、`fmt=` で決定されます。

`imageprops`

URL パスで指定されたビネットファイルまたはカタログエントリの、選択されたプロパティを返します。 返信構文と応答の MIME タイプについて詳しくは、[ プロパティ ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) を参照してください。 リクエスト内のその他のコマンドは無視されます。 次のプロパティが返されます。

<table id="table_A30296D29B5D43F1B5383A887252C6B4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>種類 </p> </th> 
   <th colname="col3" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.expiration </span> </p> </td> 
   <td colname="col2"> <p>ダブル </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 属性：:Expiration </span> またはデフォルトの有効期間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td colname="col2"> <p>整数 </p> </td> 
   <td colname="col3"> <p>解像度の高さ（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td colname="col2"> <p>文字列 </p> </td> 
   <td colname="col3"> <p>このビネットに関連付けられたプロファイルの名前と説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile </span> </p> </td> 
   <td colname="col2"> <p>ブール値 </p> </td> 
   <td colname="col3"> <p>関連付けられたプロファイルがビネットに埋め込まれている場合は 1。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded PhotoshopPaths </span> </p> </td> 
   <td colname="col2"> <p>ブール値 </p> </td> 
   <td colname="col3"> <p>ビネットにパスデータが埋め込まれている場合は 1。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier </span> </p> </td> 
   <td colname="col2"> <p>文字列 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 属性：:Modifier </span> またはカタログエントリでない場合は空です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td colname="col2"> <p>列挙 </p> </td> 
   <td colname="col3"> <p>レスポンスイメージのピクセルタイプ。使用できる値は、「CMYK」、「RGB」または「BW」（グレースケール画像の場合）です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td colname="col2"> <p>実数 </p> </td> 
   <td colname="col3"> <p>デフォルトの印刷解像度（dpi）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp </span> </p> </td> 
   <td colname="col2"> <p>文字列 </p> </td> 
   <td colname="col3"> <p>変更日時（カタログ：:TimeStamp </span> またはビネットファイル <span class="codeph"> より）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td colname="col2"> <p>整数 </p> </td> 
   <td colname="col3"> <p>フル解像度の幅（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.name </span> </p> </td> 
   <td colname="col2"> <p>文字列 </p> </td> 
   <td colname="col3"> <p>ビネット名（ルートビネットオブジェクトの名前文字列）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res </span> </p> </td> 
   <td colname="col2"> <p>実数 </p> </td> 
   <td colname="col3"> <p>マテリアルの解像度 </a> 単位（通常はピクセル/インチ） <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 表す最大オブジェクト解像度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg </span> </p> </td> 
   <td colname="col2"> <p>実数 </p> </td> 
   <td colname="col3"> <p>マテリアル解像度 </a> 単位 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> おける平均オブジェクト解像度（通常はピクセル/インチ <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> マテリアル解像度 </a>h）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.min </span> </p> </td> 
   <td colname="col2"> <p>実数 </p> </td> 
   <td colname="col3"> <p>マテリアルの解像度 </a> 単位（通常はピクセル/インチ） <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> おける最小オブジェクト解像度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version </span> </p> </td> 
   <td colname="col2"> <p>整数 </p> </td> 
   <td colname="col3"> <p>ビネット ファイルのバージョン番号。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

ビネットに含まれる画像マップデータを返します。 デフォルトでは、すべての一番外側のグループのマップ データが返されます。 すべての最も内側のグループのマップデータは、

`req=map&groupLevel=-1`

マップ データは、`wid=`、`hei=`、またはその他の方法で変更されたサイズに変更されません。 応答の MIME タイプは `<text/xml>` です。

レスポンスデータは、タグのHTMLに似た、一連の `<area>` 要素を含む `<map>` 要素で構成され `<AREA>` す。

各 `<area>` 要素には、標準の `type=` 属性と `coord=` 属性、およびビネット グループ名または名前パスを指定する `name=` 属性が含まれます。 対応するオブジェクトグループのマスクが不連続な領域を持つ場合、同じ名前の `<area>` 要素が複数存在します。

ビネットは、デフォルトの属性に加えて、追加の属性を定義することもできます（作成した場合）。 このようなカスタム属性は、オブジェクトグループ属性として定義されます。 カスタム属性の名前は、`<area>` 要素に含める `map` で始める必要があります。 例えば、グループ属性に `map.href=http://www.scene7.com` が含まれる場合、対応する `<area>` 要素には `href="http://www.scene7.com"` が含まれます。

ビネットにマップデータが含まれていない場合、空の `<map>` 要素を含む XML ドキュメントが返されます。

`object`

指定されたコマンドを実行し、残余オブジェクトの選択（要求の最後の `sel=` または `obj=` のコマンドで選択されたグループまたはオブジェクト）によってマスクされたレンダリング イメージを返します。 通常、アルファをサポートする画像形式で使用します（[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) を参照）。 アルファをサポートしていない画像形式を使用すると、マスクの外側の領域は黒になります。

`props`

指定されたコマンドを実行し、レンダリングされたイメージではなく、ビネット プロパティとグループまたはオブジェクト プロパティを返します。 返信構文と応答の MIME タイプについて詳しくは、[ プロパティ ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) を参照してください。 `obj=` または `sel=` も指定されていない限り、デフォルトの選択が適用されます（[`obj=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) を参照）。

応答には、次のプロパティが含まれる場合があります。

<table id="table_F3ECF0584F6247A2A75C1CAFE1C57A4E"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>プロパティ </p> </th> 
   <th class="entry"> <p> 種類 </p> </th> 
   <th class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> image.bgc </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 返信画像の背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p>整数 </p> </td> 
   <td> <p> 返信画像の高さ（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> ブール値 </p> </td> 
   <td> <p>True を指定すると、ICC プロファイルが返信画像に埋め込まれます（<span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span> を参照）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 返信画像に関連付けられたプロファイルのショートカット名（<span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span> を参照）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> ブール値 </p> </td> 
   <td> <p> 返信画像にアルファ版が含まれる場合は True を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> ブール値 </p> </td> 
   <td> <p> 返信画像にパスデータが含まれる場合は、true を指定します（<span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span> を参照）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 返信画像のタイプは、「CMYK」、「RGB」または「BW」（グレースケール画像の場合）にすることができます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> 実数 </p> </td> 
   <td> <p> 印刷解像度（dpi） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p>整数、ブール </p> </td> 
   <td> <p> JPEGの画質とクロマフラグ（<span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span> を参照） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 返信画像の MIME タイプ（<span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span> を参照）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 返信画像の幅（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 現在の選択範囲の属性文字列。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.count </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 現在の選択範囲内にあるオブジェクトの数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.ident </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 現在の選択範囲のインデント値。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes </span>ion.name </span> を選択してくださ <span class="codeph">。 </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 現在のオブジェクト選択のフルネームのパス。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.overlapping </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 現在選択されているオブジェクトのオーバーラップ数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p>現在の選択範囲内にあるレンダリング可能なオブジェクトの数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.texturable </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 現在選択されているテキスト編集可能オブジェクトの数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.visible </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 現在の選択の現在の表示/非表示ステータス。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 現在の選択範囲内の最初のオーバーラップ オブジェクトの Z オーダー値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

`vignette::UserData` のコンテンツを返します。 サーバーは、`vignette::UserData` 内の `'??'` をすべて行終端文字（`<cr><lf>`）で置き換えます。 返信は、応答の MIME タイプを &lt;text/plain> に設定したテキストデータ形式になります。

URL パスで指定されたオブジェクトが有効なビネット マップ エントリに解決されない場合、または `vignette::UserData` が空の場合、返信には行終端文字（`CR/LF`）のみが含まれます。

リクエスト文字列内のその他のコマンドは無視されます。

## プロパティ {#section-e44092e190ff4f6380583e8ed6ea5b0b}

リクエストコマンド。 リクエスト文字列のどこにでも発生する可能性があります。

## 初期設定 {#section-00c593cbf1af4364b6b78812e6b93c64}

URL に画像のパスや修飾子が含まれていない場合は、次のようになります。

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

それ以外の場合は、`req=img`

## 関連項目 {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) , [attribute::ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0), [vignette::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85), [Properties](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
