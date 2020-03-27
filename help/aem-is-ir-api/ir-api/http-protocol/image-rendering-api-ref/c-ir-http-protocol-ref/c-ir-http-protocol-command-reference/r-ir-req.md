---
description: リクエストのタイプ。 要求されたデータの種類を指定します。
seo-description: リクエストのタイプ。 要求されたデータの種類を指定します。
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: 9dd13338-3457-477f-96e7-3ace7266d0ab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# req{#req}

リクエストのタイプ。 要求されたデータの種類を指定します。

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
  <td class="stentry"> <p>コマンドを実行し、レンダリングイメージを返します。 </p> </td> 
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
  <td class="stentry"> <p>ビネット：:UserDataの <span class="codeph"> 内容を返します </span>。 </p> </td> 
 </tr> 
</table>

詳細な説明に特に記載がない限り、サーバはMIMEタイプ&lt;text/plain>のテキスト応答を返します。

`debug`

指定したコマンドを実行し、レンダリングイメージを返します。 エラーが発生した場合は、エラーイメージ( `attribute::ErrorImagePath`)の代わりにエラー情報とデバッグ情報が返されます。

`contents`

選択したオブジェクト属性を含む、ビネット内のオブジェクト階層のXML表現を返します。 リクエスト内の他のコマンドは無視されます。

`img`

指定したコマンドを実行し、レンダリングイメージを返します。 応答データの形式と応答のタイプは、によって決まりま `fmt=`す。

`imageprops`

URLパスで指定されたビネットファイルまたはカタログエントリの選択されたプロパティを返します。 応答の [MIMEタイプ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) と応答の構文について詳しくは、「プロパティ」を参照してください。 リクエスト内の他のコマンドは無視されます。 次のプロパティが返されます。

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
   <td colname="col3"> <p> <span class="codeph"> attribute::Expirationまた </span> はデフォルトの有効期間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td colname="col2"> <p>整数 </p> </td> 
   <td colname="col3"> <p>最大解像度の高さ（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td colname="col2"> <p>文字列 </p> </td> 
   <td colname="col3"> <p>このビネットに関連付けられているプロファイルの名前/説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile </span> </p> </td> 
   <td colname="col2"> <p>ブール値 </p> </td> 
   <td colname="col3"> <p>関連するプロファイルがビネットに埋め込まれる場合は1。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded PhotoshopPaths </span> </p> </td> 
   <td colname="col2"> <p>ブール値 </p> </td> 
   <td colname="col3"> <p>1は、ビネットによってパスデータが埋め込まれる場合です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier </span> </p> </td> 
   <td colname="col2"> <p>文字列 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Modifier。カタログエ </span> ントリでない場合は空。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td colname="col2"> <p>列挙 </p> </td> 
   <td colname="col3"> <p>応答画像のピクセルタイプ。は、「CMYK」、「RGB」または「BW」（グレースケール画像の場合）です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td colname="col2"> <p>実数 </p> </td> 
   <td colname="col3"> <p>デフォルトの印刷解像度(dpi)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp </span> </p> </td> 
   <td colname="col2"> <p>文字列 </p> </td> 
   <td colname="col3"> <p>変更日時(catalog::TimeStampま <span class="codeph"> たはビネットフ </span> ァイルから)。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> vignette.res </span> </p> </td> 
   <td colname="col2"> <p>実数 </p> </td> 
   <td colname="col3"> <p>マテリアル解像度単位での <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 最大オブジ </a> ェクト解像度（通常はピクセル/インチ）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg </span> </p> </td> 
   <td colname="col2"> <p>実数 </p> </td> 
   <td colname="col3"> <p>マテリアル解像度単位での <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 平均オ </a> ブジェクト解像度(通常はピクセル/イン <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> クマテリアル解 </a>像度h)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.min </span> </p> </td> 
   <td colname="col2"> <p>実数 </p> </td> 
   <td colname="col3"> <p>最小オブジェクト解像 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 度(マテリ </a> アル解像度単位、通常はピクセル/インチ)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version </span> </p> </td> 
   <td colname="col2"> <p>整数 </p> </td> 
   <td colname="col3"> <p>ビネットファイルのバージョン番号。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

ビネットに含まれる画像マップデータを返します。 デフォルトでは、最も外側のすべてのグループのマップデータが返されます。 すべての最も深いグループのマップデータは、

`req=map&groupLevel=-1`

マップデータは、拡大/縮小されたり、変更 `wid=` されたり `hei=` することはありません。 応答のMIMEタイプはです `<text/xml>`。

応答データは、HTMLタグと同 `<map>` 様に、要素のセ `<area>` ットを含む要素で構成され `<AREA>` ます。

各要素 `<area>` には、ビネットグ `type=` ループ名ま `coord=` たは名前パスを指定する、標準と属 `name=` 性に加えて、属性が含まれます。 対応す `<area>` るオブジェクトグループのマスクに不連続な領域が含まれる場合、同じ名前の複数の要素が存在します。

ビネットでは、デフォルトの属性に加えて、別の属性を作成した場合にも、その属性を定義できます。 このようなカスタム属性は、オブジェクトグループ属性として定義されます。 カスタム属性の名前はで始まる必要がありま `map`す。 を含め `<area>` る。 例えば、グループ属性にが含まれる場合、対 `map.href=http://www.scene7.com`応する要素が `<area>` 含まれるようになりま `href="http://www.scene7.com"`す。

ビネットにマップデータが含ま `<map>` れていない場合、空の要素を持つXMLドキュメントが返されます。

`object`

指定したコマンドを実行し、残りのオブジェクト選択(要求内の最後または最後のコマンドで選択されたグループまたはオブジェク `sel=` ト)でマ `obj=` スクされたレンダリングイメージを返します。 通常、アルファをサポートする画像形式と組み合わせて使用します( [fmt=を参照](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c))。 アルファをサポートしない画像形式を使用する場合、マスクの外側の領域は黒になります。

`props`

指定したコマンドを実行し、ビネットプロパティと、レンダリングされた画像ではなく、グループまたはオブジェクトのプロパティを返します。 応答のMIME [タイプ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) と応答の構文の説明については、「プロパティ」を参照してください。 またはが指定されていない限り、デ `obj=` フォル `sel=` トの選択が適用されます(を参照 [`obj=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a))。

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
   <td> <p>ICCプロファイルを返信画像に埋め込む場合はtrue( <span class="codeph"> iccEmbed=を参 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> 照 </a></span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 返信画像に関連付けられているプロファイルのショートカット名( <span class="codeph"><a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc=を参照 </a></span>してください)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> ブール値 </p> </td> 
   <td> <p> 返信画像にアルファが含まれる場合はtrue。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> ブール値 </p> </td> 
   <td> <p> 返信画像にパスデータが含まれる場合はtrueです( <span class="codeph"> pathEmbed=を <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> 参照して </a></span>ください)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 返信画像の種類。「CMYK」、「RGB」または「BW」（グレースケール画像の場合） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> 実数 </p> </td> 
   <td> <p> 印刷解像度(dpi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p>整数、ブール値 </p> </td> 
   <td> <p> JPEG画質とchromaフラグ( <span class="codeph"> qlt=を <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> 参照 </a></span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 返信画像のMIMEタイプ( <span class="codeph"><a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt=を参照 </a></span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 返信画像の幅（ピクセル単位） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 現在の選択の属性文字列。 </p> </td> 
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
   <td> <p> <span class="codeph"> select <span class="codeph"> selection.attributes </span>ion.name </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 現在のオブジェクト選択のフルネームパス。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.overlapping </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 現在の選択範囲内の重なり合うオブジェクトの数。 </p> </td> 
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
   <td> <p> 現在の選択の現在の表示/非表示のステータス。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 現在の選択範囲内の最初の重なりオブジェクトのZ順序の値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

の内容を返します `vignette::UserData`。 サーバは、すべてののを行終 `'??'` 端子( `vignette::UserData` ) `<cr><lf>`に置き換えます。 応答のMIMEタイプが&lt;text/plain>に設定されたテキストデータとして返信が形式設定されます。

URLパスで指定されたオブジェクトが有効なビネットマップエントリに解決されない場合、またはビネットマップが空の場合、返 `vignette::UserData` 信には線の終端文字( `CR/LF`)のみが含まれます。

要求文字列内の他のコマンドは無視されます。

## プロパティ {#section-e44092e190ff4f6380583e8ed6ea5b0b}

リクエストコマンド リクエスト文字列の任意の場所で発生する可能性があります。

## 初期設定 {#section-00c593cbf1af4364b6b78812e6b93c64}

URLに画像パスまたは修飾子が含まれていない場合は、次のようになります。

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

Otherwise, `req=img`

## 関連項目 {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) , [attribute::ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0), [vignette::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85), [Properties](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
