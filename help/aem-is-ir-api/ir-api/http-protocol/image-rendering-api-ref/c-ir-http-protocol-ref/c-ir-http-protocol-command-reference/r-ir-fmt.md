---
title: fmt
description: 返信画像の形式： クライアントに送信される画像データの画像エンコーディング形式と、HTTP応答ヘッダーの対応する応答MIME タイプを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 691c5421-0754-45ce-b454-dd0ceff47a58
TQID: 'https://experienceleague.adobe.com/m3ZesKWdK5ltybJWB9ZTOQa19Bimlu-g7xRE2OrQ-rY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 597
ht-degree: 4%

---

# fmt {#fmt}

返信画像の形式： クライアントに送信される画像データの画像エンコーディング形式と、HTTP応答ヘッダーの対応する応答MIME タイプを指定します。

` fmt= *`format`*[,[ *`pixelType`*][, *`tiffCompression`*]]`

<table id="simpletable_200779AA8D8D49A089A295AED5C98C8F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">形式</span> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>ロッシー・JPEG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpg </p> </td> 
  <td class="stentry"> <p>ロッシー・JPG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png </p> </td> 
  <td class="stentry"> <p>損失のないPNG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png-alpha </p> </td> 
  <td class="stentry"> <p>アルファチャンネル付きのロスレス PNG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif </p> </td> 
  <td class="stentry"> <p>TIFF: </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif-alpha </p> </td> 
  <td class="stentry"> <p>TIFFとアルファチャンネル： </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf </p> </td> 
  <td class="stentry"> <p>Macromedia swf ファイルに埋め込まれたLossy JPEG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf-alpha </p> </td> 
  <td class="stentry"> <p>Lossy JPEGとデフレート圧縮マスクをMacromedia swf ファイルに埋め込みます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>PDF </p> </td> 
  <td class="stentry"> <p>PDFに埋め込まれた画像。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>eps </p> </td> 
  <td class="stentry"> <p>非圧縮バイナリのカプセル化PostScript。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif </p> </td> 
  <td class="stentry"> <p>256色のGIF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif-alpha </p> </td> 
  <td class="stentry"> <p>255色とキーカラー透明度を備えたGIF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pixelType </span> </p> </td> 
  <td class="stentry"> <p>rgb </p> </td> 
  <td class="stentry"> <p>RGBの画像データを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>グレー </p> </td> 
  <td class="stentry"> <p>グレースケール画像データを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>cmyk </p> </td> 
  <td class="stentry"> <p>CMYK画像データを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> tiffCompression </span> </td> 
  <td class="stentry"> <p>除外 </p> </td> 
  <td class="stentry"> <p>非圧縮。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>lzw </p> </td> 
  <td class="stentry"> <p>LZW （Lempel-Ziv-Welch）圧縮（可逆）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>zip </p> </td> 
  <td class="stentry"> <p>圧縮を「デフレート」する（可逆）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>JPEG圧縮（非可逆）。 </p> </td> 
 </tr> 
</table>

*`pixelType`* エフェクトは、`icc=`が指定されていない場合に色空間の変換を出力します。*`pixelType`*&#x200B;に対応するデフォルトのカラープロファイルが適用されます。 カラーマネジメントが無効になっている場合は、ナイーブ変換が適用されます。*`pixelType`* 出力ピクセルタイプを決定する`icc=`が指定されている場合、は無視されます。

*`compression`* tif、tif-alpha、またはPDFが&#x200B;*`format`*&#x200B;として指定されている場合にのみ許可されます。 これらの画像形式でサポートされる圧縮オプションについては、次の表を参照してください。

`qlt-` JPEG、JPEG圧縮を使用したTIFF、JPEG圧縮を使用したPDF、およびSWF ファイルのJPEG エンコーディングオプションを設定します。 `fmt=gif`または`fmt=gif-alpha`の場合は`quantize=`を使用します。 詳しくは、コマンドの説明を参照してください。 他の形式には設定可能なオプションはありません。

すべての形式とピクセルタイプに対して、ピクセルコンポーネントあたり8 ビットが返されます。

次の表に、*`format`*&#x200B;と&#x200B;*`pixelType`*&#x200B;の有効な組み合わせ、対応するHTTP応答MIME タイプ、ICC プロファイルを埋め込めるかどうか（[iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)を参照）、および適用できる形式固有のオプションコマンドを示します。

<table id="table_3461A367632E4B5A8AB578850A439024"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> <span class="varname">形式</span> </p> </th> 
   <th colname="col2" class="entry"> <p> <span class="varname"> pixelType </span> </p> </th> 
   <th colname="col3" class="entry"> <p>応答MIME タイプ </p> </th> 
   <th colname="col4" class="entry"> <p>ICC プロファイルを埋め込む </p> </th> 
   <th colname="col5" class="entry"> <p>オプション </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>jpeg, jpg </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <span class="codeph"> qlt= </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb、グレー </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> （none|lzw|zip|jpeg）, pathEmbed=, qlt </span> </p> <p>（<span class="codeph"> qlt= </span>は、<span class="varname"> tiffCompression </span>が'jpeg'に設定されていない限り無視されます）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>swf, swf-alpha </p> </td> 
   <td colname="col2"> <p>rgb、グレー </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>いいえ </p> <p>（Flash Playerでは、埋め込まれたICC プロファイルは無視されます）。 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>、<span class="codeph">属性：:TrustedDomains </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>PDF </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> （none|zip|jpeg）,qlt= </span> </p> <p> （<span class="codeph"> qlt= </span>は、<span class="varname"> tiffCompression </span>が'jpeg'に設定されていない限り無視されます）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eps </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb、グレー </p> <p>（データは、グレーまたはrgbに変換した後にパレットに変換されます）。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>いいえ </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

クライアントに送信される返信画像データのエンコーディング形式と、HTTP返信ヘッダーの対応する応答MIME タイプを指定します。

`png-alpha`は関連付けられていないアルファを返します（つまり、アルファはピクセル値を事前に乗算しません）。`tif-alpha`および`swf-alpha`は関連付けられたアルファを返します（つまり、アルファ値はアルファ値を事前に乗算します）。 アルファチャンネルは、`req=img`の周辺光量補正の背景マスクの反転と、`req=object`がある場合のグループまたはオブジェクトマスクに対応します。 ネストされたIR リクエストを使用する際にアルファを適用するには、埋め込まれたIR リクエストとメインリクエストに、適切なアルファファイル形式の`fmt=`を追加します。 CMYKまたはグレースケール ICC プロファイルが`icc=`で指定されている場合、アルファデータは返されません。

## プロパティ {#section-eb12a82c69d84622bcea153dd84d95b3}

リクエスト内のどこでも発生する可能性があります。

## 初期設定 {#section-d2c2af11fa974e1a84e0c6cb7fb646fe}

*`format`*&#x200B;の既定値は`attribute::Format`で、*`tiffCompression`*&#x200B;の既定値は`attribute::TiffEncoding`です。*`pixelType`* `icc=`が指定されていない場合、デフォルトは`rgb`です。指定されていない場合は、指定されたICC プロファイルのピクセルタイプに対応します。

## 関連項目 {#section-c55efc881fc94c70bff91b870e026a7b}

[属性：：形式](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-format.md#reference-da5207242f1c4f1c8fa4df6027121ff2)、[属性：:JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)、[属性：:TiffEncoding](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-tiffencoding.md#reference-a3425191166042d59db766c468857d0e)、[qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)、[iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)、[pathEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f)、[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)、[quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)
