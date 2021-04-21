---
description: 応答画像の形式。
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 4%

---


# fmt{#fmt}

応答画像の形式。

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* —jpeg | jpg | pjpeg | png | png8 | png-alpha | png8-alpha | tif | tif-alpha | swf | swf-alpha | swf3 | swf3-alpha | eps | gif | gif-alpha | m3u8 | f4m | web | webp-alpha | jpeg2000 | jpeg2000-alpha | jpegxr | jpegxr-alpha

| *`format`* | 説明 |
|---|---| 
| `jpeg` | 非可逆圧縮JPEG |
| `jpg` | 非可逆圧縮JPG |
| `pjpeg` | プログレッシブ JPEG |
| `png` | 24ビット可逆圧縮PNG |
| `png8` | 8-bit可逆圧縮PNG |
| `png-alpha` | アルファチャネル付き24ビット可逆圧縮PNG |
| `png8-alpha` | アルファチャネル付き8ビット可逆圧縮PNG |
| `tif` | TIFF |
| `tif-alpha` | アルファチャネルのTIFF |
| `pdf` | PDFに埋め込まれた画像 |
| `eps` | 非圧縮バイナリEncapsulated PostScript |
| `gif` | 2 ～ 256色のGIF |
| `gif-alpha` | キーカラーの透明部分がプラスされた2 ～ 255色のGIF |
| `swf` | AdobeAS2 swfファイルに埋め込まれた非可逆圧縮JPEG |
| `swf-alpha` | 非可逆圧縮JPEGおよびAdobeAS2 swfファイルに埋め込まれたデフレート圧縮マスク |
| `swf3` | AdobeAS3 swfファイルに埋め込まれた非可逆圧縮JPEG |
| `swf3-alpha` | 非可逆圧縮JPEGと、AdobeAS3 swfファイルに埋め込まれた圧縮マスク。 **注意**:swfおよびswf-alpha形式は、ActionScript2アプリケーション(Flash Player8以前)に最適です。ActionScript3アプリケーション(Flash Player9以降)には、swf3およびswf3-alphaを使用することをお勧めします。 |
| `m3u8` | Apple Streaming Serverマニフェスト形式 |
| `f4m` | Flashストリーミングサーバのマニフェスト形式 |
| `webp` | 非可逆圧縮WebP |
| `webp-alpha` | アルファチャネルを備えた非可逆および非可逆のWebP |
| `jpeg2000` | 非可逆圧縮JPEG 2000 |
| `jpeg2000-alpha` | 非可逆圧縮JPEG 2000(アルファチャネル) |
| `jpegxr` | 非可逆圧縮JPEG XR |
| `jpegxr-alpha` | 非可逆および非可逆のアルファチャネルのJPEG XR |


| *`pixelType`* — rgb | 灰色 | cmyk |
| *`pixelType`* | 説明 |
|---|---|
| `rgb` | RGB画像データを返します。 |
| `gray` | グレースケールの画像データを返します。 |
| `cmyk` | CMYK画像データを返します。 |

| *`compression`* — none | lzw | zip | jpeg | 非可逆 | 可逆 |
| *`compression`* | 説明 |
|---|---|
| `none` | 非圧縮 |
| `lzw` | LZW(Lempel-Ziv-Welch)圧縮（可逆圧縮） |
| `zip` | 「Deflate」圧縮（可逆圧縮） |
| `jpeg` | JPEG圧縮（非可逆圧縮） |
| `lossy` | WebP、JPEG 2000、およびJPEG XR圧縮（非可逆圧縮） |
| `lossless` | WebP、JPEG 2000、およびJPEG XR圧縮（可逆圧縮） |

* *`format`* クライアントに送信する画像データの画像エンコーディング形式と、HTTP応答ヘッダーの対応する応答MIMEタイプを指定します。
* *`pixelType`* を指定しない場合は、出力カラースペースの変換を行うた `icc=` めに使用できます。

   *`pixelType`*&#x200B;に対応するデフォルトのカラープロファイルが適用されます。 カラーマネジメントが無効になっている場合は、純粋な変換が適用されます。 *`pixelType`* を指定した場合は無視され `icc=` 、出力ピクセルタイプが決定されます。

* *`compression`* は、 `tif`、、、 `tif-alpha`、 `pdf`、 `webp`、、、 `webp-alpha` `jpeg2000`、 `jpeg2000-alpha`、 `jpegxr`、 `jpegxr-alpha` 、 *`format`*、、、、や、、を、として指定した場合にのみ使用できます。これらの画像形式でサポートされる圧縮オプションについては、次の表を参照してください。

`qlt=`を使用して、次の形式のJPEGエンコーディングオプションを設定できます。JPEG、TIFF（JPEG圧縮時）、PDF（JPEG圧縮時）およびSWF。 WebP、JPEG 2000、およびJPEG XRでも`qlt=`が使用されますが、値によって、形式ごとに異なるクォリティが得られます。 `fmt=gif`または`fmt=gif-alpha`の場合は`quantize=`を使用します。 詳細については、コマンドの説明を参照してください。 その他の形式では、設定可能なオプションはありません。

すべての&#x200B;*`formats`*&#x200B;と&#x200B;*`pixelTypes`*&#x200B;に対して、8ビット/ピクセルコンポーネントが返されます（GIFの場合は8ビット/ピクセル）。

次の表は、*`format`*と&#x200B;*`pixelType`*&#x200B;の有効な組み合わせ、対応するHTTP応答のMIMEタイプ、ICCプロファイルを埋め込めるかどうか（[iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)を参照）、および適用できる形式固有のオプションをリストしています。

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> 形式</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b> 応答のMIMEタイプ</b> </th> 
   <th class="entry"> <b>ICCプロファイルを埋め込む</b> </th> 
   <th class="entry"> <b> オプション</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg、jpg、pjpeg </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span>、 <span class="codeph"> pscan=  </span>、 <span class="codeph"> qlt=  </span>、 <span class="codeph"> xmpEmbed=  </span> </p> <p><span class="codeph"> pscan= </span>パラメーターは、pjpeg形式にのみ適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png、png-alpha </p> </td> 
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
   <td colname="col5"> <span class="codeph"> <span class="varname"> 圧縮  </span> </span> <p> ( <span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>'tiff'のみ「tiff-alpha」はjpeg圧縮をサポートしていません。 </p> <p> <span class="codeph"> qlt=  </span> </p> <p> <span class="codeph"> 圧縮 </span> が <span class="varname"> jpegに設定されていない場合、qlt= </span> は無視され <span class="codeph">  </span>ます。 </p> <p>, pathEmbed=、xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf, swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb、グレー </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>いいえ </p> <p> <p>注意： AdobeFlash Playerは、埋め込まれたICCプロファイルを無視します。 </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>、 <span class="codeph"> attribute::TrustedDomains  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> PDF </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 圧縮  </span> </span> <p> ( <span class="codeph"> none|zip|jpeg </span>)、<span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> 圧縮 </span> が <span class="codeph"> <span class="varname"> jpegに設定されていない場合、qlt= </span> </span> は無視され <span class="codeph">  </span>ます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> gif、gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb、グレー </p> <p>グレーまたはRGBに変換したデータはパレットに変換されます。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>いいえ </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> 量子化=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>web、webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>いいえ </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> 圧縮 </span> </span> ( <span class="codeph"> 非可逆、 </span>非可逆 <span class="codeph">  </span>) </p> <p> <span class="codeph"> qlt= </span> は <span class="codeph"> 可逆圧縮では無視され </span>ます。 </p> <p>WebP形式のクロミナンスダウンサンプリングの概念がないので、<span class="codeph"> qlt </span>で2番目の値を使用する場合（例えば、<span class="codeph"> qlt=80,1 </span>）、2番目の値(<span class="codeph"> 1 </span>)は無視されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000、jpeg2000-alpha </p> </td> 
   <td> <p>rgb、グレー </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>いいえ </p> </td> 
   <td> <p>上記と同じ。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxr、jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>いいえ </p> </td> 
   <td> <p>上記と同じ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

要求属性。 `req=img`（デフォルト）または`req=mask`の場合は、現在のレイヤー設定に関係なく適用されます。それ以外の場合は無視されます。

*`type`* を指定した場合は無視 `iccProfile=` されます。

## 初期設定 {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`。この場合、 *`defaultType`* は次のように処理されます。を指定 `icc=` した場合、は指定したICCプロファイルのピクセルタイプ *`defaultType`* に対応します。`icc=`を指定しない場合、*`defaultType`*&#x200B;は`gray` if `req=mask`、それ以外の場合は`rgb`です。

## 例 {#section-b93222e652df404a84c69025247f07df}

**小さい低画質のプレビュー画像をJPEG形式で要求します（デフォルト）。**

` http:// *`server`*/myRootId/myImageId?qlt=60&wid=200`

**グレースケールに変換した同じ画像を要求します。**

` http:// *`server`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**同じ画像を、アルファチャネルと高解像度の可逆圧縮形式で要求します。**

` http:// *`server`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**グレースケールのTIFF画像と同じ画像に対して、アルファチャネルを要求します。**

` http:// *`server`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**初期設定のICCプロファイルを使用して、同じ画像をcmykに変換します。**

` http:// *`server`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**別のICCプロファイルを使用して同じ画像をcmykに変換し、プロファイルをTIFF画像に埋め込みます。**

` http:// *`server`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**この画像をTIFファイルとして、ピクセルタイプ変換なしでJPEG圧縮を使用して配信します。**

` http:// *`server`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**キーカラーの透明部分を持つバイトナルGIFに画像を変換し、カラーを白黒に強制的に変換します。**

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**画質設定が80の非可逆圧縮：**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**アルファ付き可逆圧縮：**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**画質設定が80の非可逆圧縮：**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**アルファ付き可逆圧縮：**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**画質設定が80の非可逆圧縮：**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**アルファ付き可逆圧縮：**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## 関連項目 {#section-fce8d69c74234bf48cf814d799409541}

[lt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) q [untize=, quantize=, quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)req=,  [quantize=req=, icc, iccEmbed=, icc ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)pathEmbed=ped, pscan pscan  [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135)leq
