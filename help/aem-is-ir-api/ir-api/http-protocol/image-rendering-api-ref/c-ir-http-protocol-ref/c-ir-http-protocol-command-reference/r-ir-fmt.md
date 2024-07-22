---
title: fmt
description: 返信画像の形式。 クライアントに送信する画像データの画像エンコード形式と、HTTP 応答ヘッダーに対応する応答の MIME タイプを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 691c5421-0754-45ce-b454-dd0ceff47a58
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 4%

---

# fmt {#fmt}

返信画像の形式。 クライアントに送信する画像データの画像エンコード形式と、HTTP 応答ヘッダーに対応する応答の MIME タイプを指定します。

` fmt= *`format`*[,[ *`pixelType`*][, *`tiffCompression`*]]`

<table id="simpletable_200779AA8D8D49A089A295AED5C98C8F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 形式 </span> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>非可逆JPEG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpg </p> </td> 
  <td class="stentry"> <p>非可逆JPG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png </p> </td> 
  <td class="stentry"> <p>損失のない PNG </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png-alpha </p> </td> 
  <td class="stentry"> <p>アルファチャンネル付きロスレス PNG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif </p> </td> 
  <td class="stentry"> <p>TIFF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif-α </p> </td> 
  <td class="stentry"> <p>アルファチャンネルのTIFF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf </p> </td> 
  <td class="stentry"> <p>Macromedia swf ファイルに埋め込まれた非可逆JPEG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf-alpha </p> </td> 
  <td class="stentry"> <p>Macromedia swf ファイルに埋め込まれた非可逆JPEGおよび圧縮済みマスク。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>PDF </p> </td> 
  <td class="stentry"> <p>PDFに埋め込まれた画像。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>eps </p> </td> 
  <td class="stentry"> <p>非圧縮バイナリでカプセル化されたPostScript。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif </p> </td> 
  <td class="stentry"> <p>256 色のGIF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif-alpha </p> </td> 
  <td class="stentry"> <p>255 色とキーカラーの透明度を備えたGIF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pixelType</span> </p> </td> 
  <td class="stentry"> <p>rgb </p> </td> 
  <td class="stentry"> <p>RGBの画像データを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>グレー </p> </td> 
  <td class="stentry"> <p>グレースケールの画像データを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>cmyk </p> </td> 
  <td class="stentry"> <p>CMYK 画像データを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> tiffCompression </span> </td> 
  <td class="stentry"> <p>除外 </p> </td> 
  <td class="stentry"> <p>非圧縮。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>lzw </p> </td> 
  <td class="stentry"> <p>LZW （Lempel-Ziv-Welch）圧縮（ロスレス） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>zip </p> </td> 
  <td class="stentry"> <p>「圧縮を圧縮する」（可逆圧縮） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>JPEG圧縮（非可逆）。 </p> </td> 
 </tr> 
</table>

`icc=` が指定されていない場合、*`pixelType`* Effects はカラースペース変換を出力します。*`pixelType`* に対応するデフォルトのカラープロファイルが適用されます。 カラーマネジメントが無効の場合、ネイティブ変換が適用されます。 *`pixelType`* `icc=` が指定されている場合、出力ピクセルのタイプを決定する無視されます。

*`compression`* tif、tif-alpha、またはPDFが *`format`* として指定されている場合にのみ使用できます。 これらの画像形式でサポートされる圧縮オプションについては、次の表を参照してください。

`qlt-`JPEG、JPEG圧縮を使用したPDF、JPEG圧縮を使用したTIFF、SWFファイルなどのJPEGエンコーディングオプションを設定します。 `fmt=gif` または `fmt=gif-alpha` の場合は `quantize=` を使用します。 詳細は、コマンドの説明を参照してください。 その他の形式には、設定可能なオプションはありません。

すべての形式およびピクセルタイプで、1 ピクセルあたり 8 ビットのコンポーネントが返されます。

次の表に、*`format`* と *`pixelType`* の有効な組み合わせ、対応する HTTP 応答の MIME タイプ、ICC プロファイルを埋め込むことができるかどうか（[iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) を参照）、および適用できる形式固有のオプションコマンドを示します。

<table id="table_3461A367632E4B5A8AB578850A439024"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> <span class="varname"> 形式 </span> </p> </th> 
   <th colname="col2" class="entry"> <p> <span class="varname"> pixelType</span> </p> </th> 
   <th colname="col3" class="entry"> <p>応答の MIME タイプ </p> </th> 
   <th colname="col4" class="entry"> <p>ICC プロファイルを埋め込む </p> </th> 
   <th colname="col5" class="entry"> <p>オプション </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>jpeg, jpg </p> </td> 
   <td colname="col2"> <p>rgb, グレー，cmyk </p> </td> 
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
   <td colname="col1"> <p>tif、tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, グレー，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> （none|lzw|zip|jpeg）, pathEmbed=, qlt </span> </p> <p>（<span class="codeph"> qlt= </span> は、tiffCompression </span> が「jpeg」 <span class="varname"> 設定されている場合を除いて無視されます）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>swf, swf-alpha </p> </td> 
   <td colname="col2"> <p>rgb、グレー </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>いいえ </p> <p>（Flash Playerは、埋め込まれた ICC プロファイルを無視します）。 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>、<span class="codeph"> 属性：:TrustedDomains </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>PDF </p> </td> 
   <td colname="col2"> <p>rgb, グレー，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> （なし|zip|jpeg）,qlt= </span> </p> <p> （<span class="codeph"> qlt= </span> は、tiffCompression </span> が「jpeg」 <span class="varname"> 設定されている場合を除いて無視されます）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eps </p> </td> 
   <td colname="col2"> <p>rgb, グレー，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gif, gif アルファ </p> </td> 
   <td colname="col2"> <p>rgb、グレー </p> <p>（データは、グレーまたは rgb への変換後、パレットに変換されます）。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>いいえ </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

クライアントに送信される返信画像データのエンコード形式と、HTTP 返信ヘッダーに対応する応答 MIME タイプを指定します。

`png-alpha` 関連付けられていないアルファ（つまり、アルファがピクセル値をあらかじめ乗算しない）を返し、`tif-alpha` と関連付けられ `swf-alpha` アルファ（つまり、アルファ値がアルファ値にあらかじめ乗算された）を返します。 アルファ チャンネルは、ビネットの背景マスクの反転に対応します。`req=img` の場合は、グループまたはオブジェクトのマスクに対応し `req=object` す。 ネストされた赤外線要求を使用するときにアルファを適用するには、埋め込まれた赤外線要求およびメイン要求に適切なアルファ ファイル形式の `fmt=` を追加します。 CMYK またはグレースケール ICC プロファイルが `icc=` で指定されている場合、アルファ値は返されません。

## プロパティ {#section-eb12a82c69d84622bcea153dd84d95b3}

リクエスト内のどこでも発生する可能性があります。

## 初期設定 {#section-d2c2af11fa974e1a84e0c6cb7fb646fe}

*`format`* デフォルト値は `attribute::Format` で、*`tiffCompression`* デフォルト値は `attribute::TiffEncoding` です。 *`pixelType`* `icc=` が指定されていない場合は、デフォルトで `rgb` に設定されます。それ以外の場合は、指定された ICC プロファイルのピクセルタイプに対応します。

## 関連項目 {#section-c55efc881fc94c70bff91b870e026a7b}

[attribute::Format](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-format.md#reference-da5207242f1c4f1c8fa4df6027121ff2) , [attribute::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50), [attribute::TiffEncoding](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-tiffencoding.md#reference-a3425191166042d59db766c468857d0e), [qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), [pathEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb), [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)
