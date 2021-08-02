---
description: 応答画像形式。
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
source-git-commit: 9d86f2acad638cbbcb80b48ead73443c76c895a9
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 4%

---

# fmt{#fmt}

応答画像形式。

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* - avif-alpha | avif | eps | f4m | gif-alpha | gif | jpeg | jpeg2000-alpha | jpeg2000 | jpegxr-alpha | jpegxr | jpg | m3u8 | pdf | pjpeg | png-alpha | png | png8-alpha | png8 | swf-alpha | swf | swf3-alpha | swf3 | tif-alpha | tif | web-alpha | webp

| *`format`* | 説明 |
|---|---|
| `avif-alpha` | アルファチャンネル付きの非可逆および非可逆AVIF。 |
| `avif` | 非可逆および可逆AVIF。 |
| `eps` | 非圧縮バイナリEncapsulated PostScript。 |
| `f4m` | Flashストリーミングサーバのマニフェスト形式。 |
| `gif-alpha` | 2～255色とキーカラーの透明度を加えたGIF |
| `gif` | 2～256色のGIF。 |
| `jpeg` | 非可逆JPEG |
| `jpeg2000-alpha` | アルファチャンネル付き非可逆JPEG 2000 |
| `jpeg2000` | 非可逆および可逆JPEG 2000。 |
| `jpegxr-alpha` | アルファチャンネル付きの非可逆JPEG XR。 |
| `jpegxr` | 可逆および可逆JPEG XR。 |
| `jpg` | 非可逆JPG |
| `m3u8` | Apple Streaming Serverマニフェスト形式。 |
| `pdf` | PDFに埋め込まれた画像。 |
| `pjpeg` | プログレッシブ JPEG. |
| `png-alpha` | アルファチャンネル付きの24ビット可逆PNG |
| `png` | 24ビット可逆PNG |
| `png8-alpha` | アルファチャンネル付き8ビット可逆PNG |
| `png8` | 8ビット可逆PNG。 |
| `swf-alpha` | AdobeAS2 swfファイルに埋め込まれた可逆JPEGおよびデフレート圧縮マスク。 |
| `swf` | AdobeAS2 swfファイルに埋め込まれた非可逆JPEG。 |
| `swf3-alpha` | AdobeAS3 swfファイルに埋め込まれた可逆JPEGおよびデフレート圧縮マスク。 **注意：** swfおよびswf-alpha形式は、ActionScript2アプリケーション(Flash Player8以前)に最適です。ActionScript3アプリケーション(Flash Player9以降)では、swf3およびswf3-alphaの形式を使用することをお勧めします。 |
| `swf3` | AdobeAS3 swfファイルに埋め込まれた非可逆JPEG。 |
| `tif-alpha` | アルファチャンネル付きTIFF |
| `tif` | TIFF. |
| `webp-alpha` | アルファチャンネル付きの非可逆WebP。 |
| `webp` | 非可逆WebPおよび可逆WebP |

| *`pixelType`* – rgb | 灰色 | cmyk |
| *`pixelType`* | 説明 |
|---|---|
| `cmyk` | CMYK画像データを返します。 |
| `gray` | グレースケールの画像データを返す。 |
| `rgb` | RGB画像データを返します。 |

| *`compression`* – none | lzw | zip | jpeg | 非可逆 | 可逆 |
| *`compression`* | 説明 |
|---|---|
| `jpeg` | JPEG圧縮（非可逆）。 |
| `lossy` | WebP、JPEG 2000およびJPEG XR圧縮（非可逆）。 |
| `lossless` | WebP、JPEG 2000およびJPEG XR圧縮（可逆）。 |
| `lzw` | LZW(Lempel-Ziv-Welch)圧縮（可逆）。 |
| `none` | 非圧縮. |
| `zip` | 「デフレート」圧縮（可逆）。 |

* *`format`* は、クライアントに送信される画像データの画像エンコーディング形式と、HTTP応答ヘッダーに対応する応答MIMEタイプを指定します。
* *`pixelType`* を使用すると、が指定されていない場合に出力カラースペースの変 `icc=` 換がおこなわれます。

   *`pixelType`*&#x200B;に対応するデフォルトのカラープロファイルが適用されます。 カラーマネジメントが無効になっている場合、純粋な変換が適用されます。 *`pixelType`* を指定した場合は無視 `icc=` され、出力ピクセルタイプが決定されます。

* *`compression`* は、 `tif`、 `tif-alpha`、 `pdf`、 `webp`、 `webp-alpha`、 `jpeg2000`、 `jpeg2000-alpha`、 `jpegxr`、 `jpegxr-alpha`  *`format`*&#x200B;が指定されている場合にのみ使用できます。これらの画像形式でサポートされる圧縮オプションについては、以下の表を参照してください。

`qlt=`を使用して、次の形式のJPEGエンコーディングオプションを設定できます。JPEG、JPEG圧縮のTIFF、JPEG圧縮のPDFおよびSWF。 WebP、JPEG 2000、JPEG XRも`qlt=`を使用しますが、値によって形式が異なると、画質も異なります。 `fmt=gif`または`fmt=gif-alpha`の場合は`quantize=`を使用します。 詳しくは、コマンドの説明を参照してください。 その他の形式には、設定可能なオプションはありません。

すべての&#x200B;*`formats`*&#x200B;と&#x200B;*`pixelTypes`*（GIFの場合は8 bit/pixel）に対して、1ピクセルあたり8 bitが返されます。

次の表に、*`format`*と&#x200B;*`pixelType`*&#x200B;の有効な組み合わせ、対応するHTTP応答のMIMEタイプ、ICCプロファイルを埋め込めるかどうか（[iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)を参照）、適用できる形式固有のオプションを示します。

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> 形式</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b> 応答のMIMEタイプ</b> </th> 
   <th class="entry"> <b>Embed ICC profile</b> </th> 
   <th class="entry"> <b> オプション</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg、jpg、pjpeg </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span>、 pscan=  <span class="codeph"> 、  </span>qlt=  <span class="codeph"> 、  </span> <span class="codeph"> xmpEmbed=  </span> </p> <p><span class="codeph"> pscan= </span>パラメーターはpjpeg形式にのみ適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb、グレー </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> tif、tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 圧縮  </span> </span> <p> ( <span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>'tiff'のみ「tiff-alpha」はjpeg圧縮をサポートしていません。 </p> <p> <span class="codeph"> qlt=  </span> </p> <p> <span class="codeph"> 圧縮がjpegに設定され </span> ていない場合、qlt= <span class="varname"> は </span> 無視さ <span class="codeph"> れま </span>す。 </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf, swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb、グレー </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>いいえ </p> <p> <p>注意： AdobeFlash Playerは、埋め込みICCプロファイルを無視します。 </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt=  </span>、  <span class="codeph"> attribute::TrustedDomains  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> PDF </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 圧縮  </span> </span> <p> ( <span class="codeph"> none|zip|jpeg </span>)、<span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> 圧縮がjpegに設定され </span> ていない場合、qlt= <span class="codeph"> <span class="varname"> は </span> </span> 無視さ <span class="codeph"> れま </span>す。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb、グレー </p> <p>グレーまたはRGBに変換した後、データがパレットに変換されます。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>いいえ </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> quantize=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>webp, webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>いいえ </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> 圧縮 </span> </span> (非可 <span class="codeph"> 逆、可 </span>逆 <span class="codeph">  </span>) </p> <p> <span class="codeph"> qlt=は可逆 </span> では無視さ <span class="codeph"> れま </span>す。 </p> <p>WebP形式のクロミナンスダウンサンプリングの概念がないので、<span class="codeph"> qlt </span>で2番目の値（例えば、<span class="codeph"> qlt=80,1 </span>）を使用すると、2番目の値( <span class="codeph"> 1 </span>)は無視されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000、jpeg2000-alpha </p> </td> 
   <td> <p>rgb、グレー </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>いいえ </p> </td> 
   <td> <p>上記と同じ。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>いいえ </p> </td> 
   <td> <p>上記と同じ。 </p> </td> 
  </tr>
  <tr valign="top"> 
   <td> <p> avif、avif-alpha </p> </td> 
   <td> <p>rgb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>いいえ </p> </td> 
   <td> <p>上記と同じ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

リクエスト属性。 `req=img` （デフォルト）または`req=mask`の場合、現在の画層設定に関係なく適用されます。それ以外の場合は無視されます。

*`type`* が指定されている場合、は無 `iccProfile=` 視されます。

## 初期設定 {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`。は次のよ *`defaultType`* うに処理されます。を指定 `icc=` した場合、 *`defaultType`* は指定したICCプロファイルのピクセルタイプに対応します。`icc=`を指定しない場合、*`defaultType`*&#x200B;は`gray`（`req=mask`の場合）、それ以外の場合は`rgb`です。

## 例 {#section-b93222e652df404a84c69025247f07df}

**JPEG形式の小さな低画質のプレビュー画像を要求します（デフォルト）。**

` http:// *`server`*/myRootId/myImageId?qlt=60&wid=200`

**グレースケールに変換された同じ画像をリクエストします。**

` http:// *`server`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**アルファチャンネルと高解像度を使用して、同じ画像をロスレス形式でリクエストします。**

` http:// *`server`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**グレースケールのTIFF画像と同じ画像のアルファチャンネルを要求します。**

` http:// *`server`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**デフォルトのICCプロファイルを使用して、同じ画像をcmykに変換します。**

` http:// *`server`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**別のICCプロファイルを使用して同じ画像をcmykに変換し、そのプロファイルをTIFF画像に埋め込みます。**

` http:// *`server`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**この画像を、ピクセルタイプの変換を行わずにJPEG圧縮を使用してTIFファイルとして配信します。**

` http:// *`server`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**キーカラーの透明度とカラーを白黒に強制的に設定して、画像をバイトナルGIFに変換します。**

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**画質設定80の非可逆**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**アルファ付き可逆圧縮：**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**画質設定80の非可逆**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**アルファ付き可逆圧縮：**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**画質設定80の非可逆**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**アルファ付き可逆圧縮：**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## 関連項目 {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) 、 [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)、 [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、 [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)、 [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)、 [pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301)、 [pscan](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135)。
