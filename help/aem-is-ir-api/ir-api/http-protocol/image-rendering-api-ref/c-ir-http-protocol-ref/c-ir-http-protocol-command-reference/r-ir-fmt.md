---
description: 返信画像の形式。 クライアントに送信される画像データの画像エンコーディング形式と、HTTP応答ヘッダーの対応する応答MIMEタイプを指定します。
seo-description: 返信画像の形式。 クライアントに送信される画像データの画像エンコーディング形式と、HTTP応答ヘッダーの対応する応答MIMEタイプを指定します。
seo-title: fmt
solution: Experience Manager
title: fmt
topic: Scene7 Image Serving - Image Rendering API
uuid: 7c589119-d1b3-460f-acbd-5e8d10d0d976
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# fmt{#fmt}

返信画像の形式。 クライアントに送信される画像データの画像エンコーディング形式と、HTTP応答ヘッダーの対応する応答MIMEタイプを指定します。

` fmt= *``*[,[ *``*][, *`formatpixelTypetiffCompression`*`]

<table id="simpletable_200779AA8D8D49A089A295AED5C98C8F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> フォーマット </span> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>非可逆JPEG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpg </p> </td> 
  <td class="stentry"> <p>非可逆JPG </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png </p> </td> 
  <td class="stentry"> <p>可逆圧縮PNG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png-alpha </p> </td> 
  <td class="stentry"> <p>アルファチャンネル付きの可逆圧縮PNG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif </p> </td> 
  <td class="stentry"> <p>TIFF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif-alpha </p> </td> 
  <td class="stentry"> <p>アルファチャンネル付きTIFF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf </p> </td> 
  <td class="stentry"> <p>Macromedia swfファイルに埋め込まれた非可逆JPEG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf-alpha </p> </td> 
  <td class="stentry"> <p>非可逆圧縮JPEGと、Macromedia swfファイルに埋め込まれたデフレート圧縮マスク。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>PDF </p> </td> 
  <td class="stentry"> <p>PDFに埋め込まれた画像。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>eps </p> </td> 
  <td class="stentry"> <p>非圧縮バイナリEncapsulated PostScript。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif </p> </td> 
  <td class="stentry"> <p>256色のGIF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif-alpha </p> </td> 
  <td class="stentry"> <p>255色とキーカラーの透明部分を含むGIF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pixelType </span> </p> </td> 
  <td class="stentry"> <p>rgb </p> </td> 
  <td class="stentry"> <p>RGB画像データを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>灰色 </p> </td> 
  <td class="stentry"> <p>グレースケールの画像データを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>cmyk </p> </td> 
  <td class="stentry"> <p>CMYK画像データを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> tiffCompression </span> </td> 
  <td class="stentry"> <p>除外 </p> </td> 
  <td class="stentry"> <p>非圧縮. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>lzw </p> </td> 
  <td class="stentry"> <p>LZW(Lempel-Ziv-Welch)圧縮（可逆圧縮）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>zip </p> </td> 
  <td class="stentry"> <p>「Deflate」圧縮（可逆圧縮）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>JPEG圧縮（非可逆） </p> </td> 
 </tr> 
</table>

*`pixelType`* は、指定されていない場合にカラースペースの変 `icc=` 換を出力します。に対応する初期設定のカラープロファ *`pixelType`* イルが適用されます。 カラーマネジメントが無効になっている場合は、単純な変換が適用されます。 *`pixelType`* が指定された場合 `icc=` は無視され、出力ピクセルのタイプが決まります。

*`compression`* は、tif、tif-alpha、またはPDFがとして指定されている場合にのみ使用できま *`format`*&#x200B;す。 これらの画像形式でサポートされている圧縮オプションについては、次の表を参照してください。

`qlt-` は、次の形式のJPEGエンコーディングオプションを設定します。JPEG、JPEG圧縮付きTIFF、JPEG圧縮付きPDFおよびSWFファイル。 ifまたは `quantize=` を使 `fmt=gif` 用しま `fmt=gif-alpha`す。 詳細については、コマンドの説明を参照してください。 その他の形式には、設定可能なオプションはありません。

すべての形式とピクセルタイプに対して、8ビット/ピクセルコンポーネントが返されます。

次の表に、との有効な組み合わせ、対応するHTTP応 *`format`* 答のMIMEタイプ、ICCプロファイルを埋め込めるかどうか( *`pixelType`* iccEmbed= [](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f))、および適用できる形式固有のオプションコマンドを示します。

<table id="table_3461A367632E4B5A8AB578850A439024"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> <span class="varname"> フォーマット </span> </p> </th> 
   <th colname="col2" class="entry"> <p> <span class="varname"> pixelType </span> </p> </th> 
   <th colname="col3" class="entry"> <p>応答MIMEタイプ </p> </th> 
   <th colname="col4" class="entry"> <p>ICCプロファイルを埋め込む </p> </th> 
   <th colname="col5" class="entry"> <p>オプション </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>jpeg、jpg </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <span class="codeph"> qlt= </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png、png-alpha </p> </td> 
   <td colname="col2"> <p>rgb、グレー </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;画像/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png8、png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;画像/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tif、tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;画像/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> (none|lzw|zip|jpeg)、pathEmbed=、qlt </span> </p> <p>( <span class="codeph"> tiffCompressionが「jpeg」に設 </span> 定されていない場合、 <span class="varname"></span> qlt=は無視されます)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>swf、swf-alpha </p> </td> 
   <td colname="col2"> <p>rgb、グレー </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>いいえ </p> <p>（Flash Playerでは、埋め込まれたICCプロファイルは無視されます）。 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>、 <span class="codeph"> attribute::TrustedDomains </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>PDF </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> (none|zip|jpeg),qlt= </span> </p> <p> ( <span class="codeph"> tiffCompressionが「jpeg」に設 </span> 定されていない場合、 <span class="varname"></span> qlt=は無視されます)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eps </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;イメージ/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gif、gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb、グレー </p> <p>（データは、グレーまたはRGBに変換した後、パレットに変換されます）。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;イメージ/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>いいえ </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

クライアントに送信する返信画像データのエンコーディング形式と、HTTP応答ヘッダーの対応する応答MIMEタイプを指定します。

`png-alpha` は、関連付けられていないアルファを返します（つまり、alphaはピクセル値に事前に乗算されません）。一方、 `tif-alpha``swf-alpha` は関連付けられたアルファを返します（つまり、アルファ値はアルファ値と事前に乗算されます）。 アルファチャンネルは、ビネットの背景マスクの逆に対応し、の場合はグ `req=img`ループまたはオブジェクトマスクに対応します `req=object`。 ネストされたIR要求を使用する場合にアルファを適用するには、埋め込ま `fmt=` れたIR要求とメイン要求に適切なアルファファイル形式を追加します。 でCMYKまたはグレースケールICCプロファイルが指定されている場合、アルファデータは返されませ `icc=`ん。

## プロパティ {#section-eb12a82c69d84622bcea153dd84d95b3}

リクエストの任意の場所で発生する可能性があります。

## 初期設定 {#section-d2c2af11fa974e1a84e0c6cb7fb646fe}

*`format`* のデフォルトはに `attribute::Format`設定され、 *`tiffCompression`* のデフォルトはに設定されま `attribute::TiffEncoding`す。 *`pixelType`* を指定しな `rgb` い場合は、 `icc=` 初期設定がになります。それ以外の場合は、指定したICCプロファイルのピクセルタイプに対応します。

## 関連項目 {#section-c55efc881fc94c70bff91b870e026a7b}

[attribute::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-format.md#reference-da5207242f1c4f1c8fa4df6027121ff2) , [attribute::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50), [attribute::JpegQuality,](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-tiffencoding.md#reference-a3425191166042d59db766c468857d0e)::Ltiff [, lt=lt=encodingIcc Path](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)= [](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)[](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f)[](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)[encoding Path, Embed Path=Format Req Embed, Format Req](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)
