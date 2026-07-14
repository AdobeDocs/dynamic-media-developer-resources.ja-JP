---
title: req
description: リクエストタイプ： 要求されるデータのタイプを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b4a78a1-4f03-47ce-b523-10975e83f0ea
TQID: 'https://experienceleague.adobe.com/UyITy7WNd7wQzOa7UaS4xLgVfjnRwkws2sonnmbaVN0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 950
ht-degree: 3%

---

# req{#req}

リクエストタイプ： 要求されるデータのタイプを指定します。

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> デバッグ </span> </p> </td> 
  <td class="stentry"> <p>デバッグモードでコマンドを実行します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">件のコンテンツ </span> </p> </td> 
  <td class="stentry"> <p>ビネット内のオブジェクトに関する情報を返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img </span> </p> </td> 
  <td class="stentry"> <p>コマンドを実行し、レンダリングされた画像を返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">個のimageprops </span> </p> </td> 
  <td class="stentry"> <p>指定したビネットのプロパティを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> マップ </span> </p> </td> 
  <td class="stentry"> <p>周辺光量補正に埋め込まれた画像マップデータを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> オブジェクト </span> </p> </td> 
  <td class="stentry"> <p>コマンドを実行し、現在のオブジェクト選択にマスクされたレンダリング画像を返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">件の小道具</span> </p> </td> 
  <td class="stentry"> <p>コマンドを実行し、返信画像のプロパティを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ユーザーデータ </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> ビネット：:UserData </span>の内容を返します。 </p> </td> 
 </tr> 
</table>

詳細な説明に特に明記されていない限り、サーバーはMIME タイプ &lt;text/plain>のテキスト応答を返します。

`debug`

指定したコマンドを実行し、レンダリングされた画像を返します。 エラーが発生した場合、エラー画像（`attribute::ErrorImagePath`）ではなく、エラーとデバッグ情報が返されます。

`contents`

選択したオブジェクト属性を含む、ビネット内のオブジェクト階層のXML表現を返します。 リクエスト内のその他のコマンドは無視されます。

`img`

指定したコマンドを実行し、レンダリングされた画像を返します。 返信データの形式と応答の種類は`fmt=`によって決まります。

`imageprops`

URL パスで指定されたビネット ファイルまたはカタログ エントリの選択したプロパティを返します。 返信構文と応答MIME タイプの説明については、[&#x200B; プロパティ &#x200B;](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)を参照してください。 リクエスト内のその他のコマンドは無視されます。 次のプロパティが返されます。

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
   <td colname="col3"> <p> <span class="codeph">属性：：有効期限</span>、または既定の有効期間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td colname="col2"> <p>整数 </p> </td> 
   <td colname="col3"> <p>フル解像度の高さ（ピクセル単位） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td colname="col2"> <p>文字列 </p> </td> 
   <td colname="col3"> <p>このビネットに関連付けられているプロファイルの名前/説明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile </span> </p> </td> 
   <td colname="col2"> <p>ブール値 </p> </td> 
   <td colname="col3"> <p>関連するプロファイルがビネットに埋め込まれている場合は1。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded PhotoshopPaths </span> </p> </td> 
   <td colname="col2"> <p>ブール値 </p> </td> 
   <td colname="col3"> <p>周辺光量補正がパスデータを埋め込む場合は1。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier </span> </p> </td> 
   <td colname="col2"> <p>文字列 </p> </td> 
   <td colname="col3"> <p> <span class="codeph">属性：：修飾子</span>またはカタログエントリでない場合は空です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td colname="col2"> <p>列挙 </p> </td> 
   <td colname="col3"> <p>レスポンス画像のピクセルタイプ。CMYK、RGB、またはBWを指定できます（グレースケール画像の場合）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td colname="col2"> <p>実際 </p> </td> 
   <td colname="col3"> <p>Dpiのデフォルトの印刷解像度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp </span> </p> </td> 
   <td colname="col2"> <p>文字列 </p> </td> 
   <td colname="col3"> <p>変更日時（<span class="codeph"> カタログ：:TimeStamp </span>またはビネットファイルから）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td colname="col2"> <p>整数 </p> </td> 
   <td colname="col3"> <p>フル解像度の幅（ピクセル単位） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ビネット。名前</span> </p> </td> 
   <td colname="col2"> <p>文字列 </p> </td> 
   <td colname="col3"> <p>ビネット名（ルートビネットオブジェクトの名前文字列）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ビネット.res </span> </p> </td> 
   <td colname="col2"> <p>実際 </p> </td> 
   <td colname="col3"> <p>マテリアル解像度<a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local">の最大オブジェクト解像度</a>単位（通常はピクセル/インチ）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg </span> </p> </td> 
   <td colname="col2"> <p>実際 </p> </td> 
   <td colname="col3"> <p>マテリアル解像度<a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local">の平均解像度</a>単位（通常はピクセル/ピクセル数<a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> マテリアル解像度</a>時間）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.min </span> </p> </td> 
   <td colname="col2"> <p>実際 </p> </td> 
   <td colname="col3"> <p>マテリアル解像度<a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local">の最小オブジェクト解像度</a>単位（通常はピクセル/インチ）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ビネット。バージョン </span> </p> </td> 
   <td colname="col2"> <p>整数 </p> </td> 
   <td colname="col3"> <p>ビネットファイルのバージョン番号。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

周辺光量補正に含まれる画像マップデータを返します。 デフォルトでは、最も外側のすべてのグループのマップデータが返されます。 すべての内部グループのマップデータは、次のコマンドを使用して取得できます

`req=map&groupLevel=-1`

マップ データが`wid=`または`hei=`に拡張されていないか、その他の方法で変更されていません。 応答MIME タイプは`<text/xml>`です。

応答データは、HTML `<AREA>` タグと同様に、`<area>`要素のセットを含む`<map>`要素で構成されます。

各`<area>`要素には、標準の`type=`および`coord=`属性と`name=`属性が含まれ、周辺光量補正グループ名または名前パスを指定します。 対応するオブジェクトグループのマスクに不連続領域がある場合、同じ名前の複数の`<area>`要素が存在します。

ビネットは、デフォルトの属性に加えて、作成された場合に追加の属性を定義できます。 このようなカスタム属性は、オブジェクトグループ属性として定義されます。 カスタム属性の名前は、`<area>`要素に含めるには`map`で始める必要があります。 例えば、グループ属性に`map.href=http://www.scene7.com`が含まれる場合、対応する`<area>`要素には`href="http://www.scene7.com"`が含まれます。

周辺光量補正にマップデータが含まれていない場合は、空の`<map>`要素を持つXML ドキュメントが返されます。

`object`

指定されたコマンドを実行し、残りのオブジェクト選択（リクエストの最後の`sel=`または`obj=` コマンドで選択されたグループまたはオブジェクト）によってマスクされたレンダリング画像を返します。 通常、アルファをサポートする画像形式で使用されます（[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)を参照）。 アルファをサポートしない画像形式を使用する場合、マスクの外側の領域は黒になります。

`props`

指定したコマンドを実行し、レンダリングされた画像ではなく、周辺光量補正プロパティとグループまたはオブジェクトのプロパティを返します。 返信構文と応答MIME タイプの説明については、[&#x200B; プロパティ &#x200B;](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)を参照してください。 デフォルトの選択は、`obj=`または`sel=`が指定されていない限り適用されます（[`obj=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)を参照）。

応答には、次のプロパティを含めることができます。

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
   <td> <p> 画像の高さをピクセル単位で返信します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> ブール値 </p> </td> 
   <td> <p>Icc プロファイルが返信画像に埋め込まれている場合はtrueです（<span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span>を参照）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 返信画像に関連付けられたプロファイルのショートカット名（<span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span>を参照）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> ブール値 </p> </td> 
   <td> <p> 返信画像にアルファが含まれる場合はTrueです。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> ブール値 </p> </td> 
   <td> <p> 返信画像にパスデータが含まれる場合はTrueです（<span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>を参照）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 返信画像の種類。CMYK、RGB、BWのいずれかです（グレースケール画像の場合） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> 実際 </p> </td> 
   <td> <p> 印刷解像度（dpi） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p>整数、ブール値 </p> </td> 
   <td> <p> JPEGの画質とクロマフラグ （<span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span>を参照） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 返信画像のMime タイプ（<span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span>を参照）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 画像の幅をピクセル単位で返信します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 現在の選択範囲の属性文字列。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">件の選択回数</span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 現在の選択範囲にあるオブジェクトの数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.ident </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 現在の選択範囲のインデント値。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> select <span class="codeph"> selection.attributes </span>ion.name </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 現在のオブジェクト選択のフルネーム パス。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">件の選択。</span>と重複しています </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 現在の選択範囲の重なりオブジェクトの数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p>現在の選択範囲のレンダリング可能なオブジェクトの数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.texturable </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 現在の選択範囲のテクスチャ可能オブジェクトの数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">件の選択。表示中</span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 現在の選択範囲の現在の表示/非表示ステータス。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 現在の選択範囲の最初の重なりオブジェクトのZ次値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

`vignette::UserData`の内容を返します。 サーバーは、`vignette::UserData`内の`'??'`のすべての出現箇所を行終端（`<cr><lf>`）に置き換えます。 返信は、応答MIME タイプが&lt;text/plain>に設定されたテキストデータとしてフォーマットされます。

URL パスで指定されたオブジェクトが有効な周辺光量補正マップエントリに解決しない場合、または`vignette::UserData`が空の場合、応答には行終端（`CR/LF`）のみが含まれます。

リクエスト文字列内の他のコマンドは無視されます。

## プロパティ {#section-e44092e190ff4f6380583e8ed6ea5b0b}

リクエストコマンド。 リクエスト文字列内の任意の場所で発生する可能性があります。

## 初期設定 {#section-00c593cbf1af4364b6b78812e6b93c64}

URLに画像パスまたは修飾子が含まれていない場合は、次の手順を実行します。

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

それ以外は、`req=img`

## 関連項目 {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)、[属性：:ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)、[周辺光量補正：:UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85)、[&#x200B; プロパティ &#x200B;](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)

