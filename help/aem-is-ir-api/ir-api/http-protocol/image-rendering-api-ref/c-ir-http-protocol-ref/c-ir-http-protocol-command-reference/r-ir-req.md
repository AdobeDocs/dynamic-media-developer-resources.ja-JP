---
title: req
description: リクエストタイプ。 リクエストするデータのタイプを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b4a78a1-4f03-47ce-b523-10975e83f0ea
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 4%

---

# req{#req}

リクエストタイプ。 リクエストするデータのタイプを指定します。

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> デバッグ </span> </p> </td> 
  <td class="stentry"> <p>デバッグモードでコマンドを実行します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 内容 </span> </p> </td> 
  <td class="stentry"> <p>ビネット内のオブジェクトに関する情報を返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img </span> </p> </td> 
  <td class="stentry"> <p>コマンドを実行し、レンダリングされたイメージを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> imageprops </span> </p> </td> 
  <td class="stentry"> <p>指定したビネットのプロパティを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> マップ </span> </p> </td> 
  <td class="stentry"> <p>ビネットに埋め込まれた画像マップデータを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> オブジェクト </span> </p> </td> 
  <td class="stentry"> <p>コマンドを実行し、現在のオブジェクト選択にマスクされたレンダリングイメージを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> prop </span> </p> </td> 
  <td class="stentry"> <p>コマンドを実行し、返信画像のプロパティを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> userdata </span> </p> </td> 
  <td class="stentry"> <p>次の内容を返します： <span class="codeph"> vignette::UserData </span>. </p> </td> 
 </tr> 
</table>

詳細な説明に特に記載がない限り、サーバーは MIME タイプを持つテキスト応答を返します &lt;text plain=&quot;&quot;>.

`debug`

指定したコマンドを実行し、レンダリングされたイメージを返します。 エラーが発生した場合、エラーイメージ ( `attribute::ErrorImagePath`) をクリックします。

`contents`

ビネット内のオブジェクト階層の XML 表現を返します。この中には、選択したオブジェクト属性も含まれます。 リクエスト内の他のコマンドは無視されます。

`img`

指定したコマンドを実行し、レンダリングされたイメージを返します。 返信データの形式と応答タイプは、 `fmt=`.

`imageprops`

URL パスで指定されたビネットファイルまたはカタログエントリの選択されたプロパティを返します。 詳しくは、 [プロパティ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) を参照してください。 リクエスト内の他のコマンドは無視されます。 次のプロパティが返されます。

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
   <td colname="col3"> <p> <span class="codeph"> attribute::Expiration </span> またはデフォルトの有効期間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td colname="col2"> <p>整数 </p> </td> 
   <td colname="col3"> <p>最大解像度の高さ（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td colname="col2"> <p>文字列 </p> </td> 
   <td colname="col3"> <p>このビネットに関連付けられたプロファイルの名前/説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile </span> </p> </td> 
   <td colname="col2"> <p>ブール値 </p> </td> 
   <td colname="col3"> <p>関連付けられたプロファイルがビネットに埋め込まれている場合は 1。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded PhotoshopPaths </span> </p> </td> 
   <td colname="col2"> <p>ブール値 </p> </td> 
   <td colname="col3"> <p>1 ビネットがパスデータを埋め込む場合。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier </span> </p> </td> 
   <td colname="col2"> <p>文字列 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Modifier </span> カタログエントリでない場合は空です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td colname="col2"> <p>Enum </p> </td> 
   <td colname="col3"> <p>応答画像のピクセルタイプ。は、「CMYK」、「RGB」または「BW」（グレースケール画像の場合）です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td colname="col2"> <p>実数 </p> </td> 
   <td colname="col3"> <p>初期設定の印刷解像度 (dpi)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp </span> </p> </td> 
   <td colname="col2"> <p>文字列 </p> </td> 
   <td colname="col3"> <p>変更日時（開始日時） <span class="codeph"> catalog::TimeStamp </span> またはビネットファイル )。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td colname="col2"> <p>整数 </p> </td> 
   <td colname="col3"> <p>最大解像度の幅（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.name </span> </p> </td> 
   <td colname="col2"> <p>文字列 </p> </td> 
   <td colname="col3"> <p>ビネット名（ルートビネットオブジェクトの名前文字列）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vinette.res </span> </p> </td> 
   <td colname="col2"> <p>実数 </p> </td> 
   <td colname="col3"> <p>での最大オブジェクト解像度 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 材料分解能 </a> 単位（通常はピクセル/インチ）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg </span> </p> </td> 
   <td colname="col2"> <p>実数 </p> </td> 
   <td colname="col3"> <p>での平均オブジェクト解像度 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 材料分解能 </a> 単位（通常はピクセル数） <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 材料分解能 </a>h) を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.min </span> </p> </td> 
   <td colname="col2"> <p>実数 </p> </td> 
   <td colname="col3"> <p>での最小オブジェクト解像度 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 材料分解能 </a> 単位（通常はピクセル/インチ）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version </span> </p> </td> 
   <td colname="col2"> <p>整数 </p> </td> 
   <td colname="col3"> <p>ビネットファイルのバージョン番号。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

ビネットに含まれる画像マップデータを返します。 デフォルトでは、最も外側にあるすべてのグループのマップデータが返されます。 すべての最も内側のグループのマップデータは、

`req=map&groupLevel=-1`

マップデータは、 `wid=` または `hei=` またはそれ以外の場合は変更されます。 応答の MIME タイプは次のとおりです。 `<text/xml>`.

応答データは、 `<map>` 一連の `<area>` 要素 (HTML `<AREA>` タグを使用します。

各 `<area>` 要素に標準を含める `type=` および `coord=` 属性、および `name=` 属性で、ビネットグループ名または名前パスを指定します。 複数 `<area>` 対応するオブジェクトグループのマスクに不連続な領域がある場合、同じ名前の要素が存在します。

デフォルトの属性に加えて、ビネットで追加の属性を定義できます（作成した場合）。 このようなカスタム属性は、オブジェクトグループ属性として定義されます。 カスタム属性の名前はで始める必要があります `map` 含まれる `<area>` 要素。 例えば、グループ属性に `map.href=http://www.scene7.com`、 `<area>` 要素を含む `href="http://www.scene7.com"`.

空の XML ドキュメント `<map>` ビネットにマップデータが含まれていない場合は、要素が返されます。

`object`

指定したコマンドを実行し、残りのオブジェクト選択（最後のオブジェクトで選択されたグループまたはオブジェクト）によってマスクされたレンダリングイメージを返します `sel=` または `obj=` コマンドを使用して )。 通常、アルファをサポートする画像形式で使用します ( [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)) をクリックします。 アルファをサポートしない画像形式を使用した場合、マスクの外側の領域は黒になります。

`props`

指定したコマンドを実行し、ビネットプロパティとグループまたはオブジェクトプロパティを返します。レンダリングされたイメージは返されません。 詳しくは、 [プロパティ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) ：返信構文と応答 MIME タイプの説明。 デフォルトの選択が適用されるのは、 `obj=` または `sel=` また、 [ `obj=` ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)) をクリックします。

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
   <td> <p>ICC プロファイルが返信画像に埋め込まれている場合は true( <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span>) をクリックします。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 返信画像に関連付けられたプロファイルのショートカット名 ( <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span>) をクリックします。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> ブール値 </p> </td> 
   <td> <p> True を指定すると、返信画像にアルファが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> ブール値 </p> </td> 
   <td> <p> 返信画像にパスデータが含まれる場合は true です ( <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>) をクリックします。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 返信画像の種類。「CMYK」、「RGB」または「BW」（グレースケール画像の場合）を指定できます </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> 実数 </p> </td> 
   <td> <p> 印刷解像度 (dpi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p>整数、ブール値 </p> </td> 
   <td> <p> JPEG品質と色度フラグ ( <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 返信画像の MIME タイプ ( <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span>) をクリックします。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 返信画像の幅（ピクセル単位） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 現在の選択範囲の属性文字列。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.count </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 現在の選択範囲内のオブジェクトの数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.ident </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 現在の選択範囲のインデント値。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 選択 <span class="codeph"> selection.attributes </span>ion.name </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 現在のオブジェクト選択のフルネームパス。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.overlapping </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 現在の選択範囲内の重複オブジェクトの数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p>現在の選択範囲内のレンダリング可能なオブジェクトの数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.texturable </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 現在の選択範囲内のテクスチャ可能なオブジェクトの数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.visible </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 現在の選択項目の現在の表示/非表示のステータス。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 現在の選択範囲の最初の重なりオブジェクトの Z 順の値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

次の内容を返します： `vignette::UserData`. サーバーは、 `'??'` in `vignette::UserData` 行終端子 ( `<cr><lf>`) をクリックします。 返信はテキストデータとして書式設定され、応答の MIME タイプはに設定されます。 &lt;text plain=&quot;&quot;>.

URL パスで指定されたオブジェクトが有効なビネットマップエントリに解決されない場合、または `vignette::UserData` が空の場合、返信にはラインターミネータ ( `CR/LF`) をクリックします。

リクエスト文字列内の他のコマンドは無視されます。

## プロパティ {#section-e44092e190ff4f6380583e8ed6ea5b0b}

リクエストコマンド。 リクエスト文字列の任意の場所で発生する場合があります。

## 初期設定 {#section-00c593cbf1af4364b6b78812e6b93c64}

URL に画像パスや修飾子が含まれていない場合、次のようになります。

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

それ以外の場合は、 `req=img`

## 関連項目 {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) , [attribute::ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0), [vignette::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85), [プロパティ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
