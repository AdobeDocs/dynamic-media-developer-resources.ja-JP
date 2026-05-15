---
title: fmt
description: 応答画像の形式。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
TQID: 'https://experienceleague.adobe.com/TZi2AdS9MK2A2WtCCJMmMRvwZ70Kdt2aeHOP--QtA4U'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 1061
ht-degree: 2%

---

# fmt{#fmt}

応答画像の形式。

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* - avif-alpha | avif | eps | f4m | gif-alpha | gif | heic | jpeg | jpeg2000-alpha | jpeg2000 | jpegxr-alpha | jpegxr | jpg | m3u8 | pdf | pdf | pjpeg | png | png8-alpha | png8 | swf-alpha | swf3-alpha | swf-alpha | web-alf |

| *`format`* | 説明 |
|---|---|
| `avif-alpha` | アルファチャンネルを使用した可逆AVIF。 |
| `avif` | 可逆無可逆AVIF。 |
| `eps` | 非圧縮バイナリのカプセル化PostScript。 |
| `f4m` | Flash Streaming Server マニフェスト形式。 |
| `gif-alpha` | 2～255色とキーカラーの透明度を備えたGIF。 |
| `gif` | GIF 2～256色。 |
| `heic` | 負け知らずのHEIC。 この形式は、サポートされていない場合、ブラウザーからデフォルトでダウンロードされます。 |
| `jpeg` | ロッシー・JPEG。 |
| `jpeg2000-alpha` | アルファチャンネルを使用したJPEG 2000の可逆性と可逆性。 |
| `jpeg2000` | ロッシー&amp;ロスレスJPEG2000。 |
| `jpegxr-alpha` | アルファチャンネルを使用した可逆および可逆JPEG XR。 |
| `jpegxr` | 可逆で可逆なJPEG XR。 |
| `jpg` | ロッシー・JPG。 |
| `m3u8` | Apple Streaming Server マニフェストフォーマット。 |
| `pdf` | PDFに埋め込まれた画像。 |
| `pjpeg` | プログレッシブJPEG。 |
| `png-alpha` | アルファチャンネル付き24 ビット可逆PNG。 |
| `png` | 24 ビット可逆PNG。 |
| `png8-alpha` | アルファチャンネル付き8 ビット可逆PNG。 |
| `png8` | 8 ビットの可逆PNG。 |
| `swf-alpha` | Lossy JPEGと、Adobe AS2 swf ファイルに埋め込まれたデフレート圧縮マスク。 |
| `swf` | Lossy JPEGをAdobe AS2 swf ファイルに埋め込む。 |
| `swf3-alpha` | Lossy JPEGと、Adobe AS3 swf ファイルに埋め込まれたデフレート圧縮マスク。 **注：** swfおよびswf-alpha形式は、ActionScript 2 アプリケーション（Flash Player 8以前）に最適です。 ActionScript3 アプリケーション（Flash Player 9以降）で使用する場合は、swf3形式とswf3-alpha形式をお勧めします。 |
| `swf3` | Lossy JPEGをAdobe AS3 swf ファイルに埋め込む。 |
| `tif-alpha` | TIFFとアルファチャンネル： |
| `tif` | TIFF: |
| `webp-alpha` | アルファチャンネルを使用した可逆および可逆WebP。 |
| `webp` | 可逆と可逆のWebP。 |

*`pixelType`* - rgb | グレー| cmyk

| *`pixelType`* | 説明 |
|---|---|
| `cmyk` | CMYK画像データを返します。 |
| `gray` | グレースケール画像データを返します。 |
| `rgb` | RGBの画像データを返します。 |

*`compression`* - jpeg |非可逆|可逆| lzw |なし| zip

| *`compression`* | 説明 |
|---|---|
| `jpeg` | JPEG圧縮（非可逆）。 |
| `lossy` | JPEG 2000、JPEG XR圧縮（非可逆）、およびWebP。 |
| `lossless` | HEIC、JPEG 2000、JPEG XR圧縮（ロスレス）、WebP。 |
| `lzw` | LZW （Lempel-Ziv-Welch）圧縮（可逆）。 |
| `none` | 非圧縮。 |
| `zip` | 圧縮を「デフレート」する（可逆）。 |

* *`format`*&#x200B;は、クライアントに送信される画像データの画像エンコーディング形式と、HTTP応答ヘッダーの対応する応答MIME タイプを指定します。
* `icc=`が指定されていない場合、*`pixelType`*&#x200B;を使用して出力カラースペースの変換を行うことができます。

  *`pixelType`*&#x200B;に対応する既定のカラープロファイルが適用されます。 カラーマネジメントが無効になっている場合は、ナイーブ変換が適用されます。 出力ピクセルの種類を決定する`icc=`が指定されている場合、*`pixelType`*&#x200B;は無視されます。

* *`compression`*&#x200B;は、`tif`、`tif-alpha`、`pdf`、`webp`、`webp-alpha`、`jpeg2000`、`jpeg2000-alpha`、`jpegxr`または`jpegxr-alpha`が&#x200B;*`format`*&#x200B;として指定されている場合にのみ許可されます。 これらの画像形式でサポートされる圧縮オプションについては、次の表を参照してください。

`qlt=`を使用して、JPEG、JPEG圧縮を使用したTIFF、JPEG圧縮を使用したPDF、SWFの形式のJPEG エンコーディングオプションを設定できます。 WebP、JPEG 2000、およびJPEG XRも`qlt=`を使用しますが、値によって異なる形式に対して異なる品質が得られます。 `fmt=gif`または`fmt=gif-alpha`の場合は`quantize=`を使用します。 詳しくは、コマンドの説明を参照してください。 他の形式には設定可能なオプションはありません。

すべての&#x200B;*`formats`*&#x200B;および&#x200B;*`pixelTypes`*&#x200B;に対して、1 ピクセルあたり8 ビットのコンポーネントが返されます（GIFの場合は1 ピクセルあたり8 ビット）。

次の表は、*`format`*と&#x200B;*`pixelType`*&#x200B;の有効な組み合わせ、対応するHTTP応答MIME タイプ、ICC プロファイルを埋め込めるかどうか（[iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)を参照）、適用できる形式固有のオプションを示しています。

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>形式</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b>応答MIME タイプ </b> </th> 
   <th class="entry"> <b>ICC プロファイルを埋め込む</b> </th> 
   <th class="entry"> <b> オプション </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> avif, avif-alpha </p> </td> 
   <td> <p>rgb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image/avif&gt; </span> </p> </td> 
   <td> <p>いいえ </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname">圧縮</span> </span> （<span class="codeph">非可逆</span>、<span class="codeph">可逆</span>） </p> <p> <span class="codeph"> qlt= </span>は、<span class="codeph">の可逆性</span>に対して無視されます。 </p> <p>WebP形式ではクロミナンスのダウンサンプリングという概念はないため、<span class="codeph"> qlt </span>の2番目の値（例：<span class="codeph"> qlt=80,1 </span>）を使用する場合、2番目の値（<span class="codeph"> 1 </span>）は無視されます。 </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb、グレー </p> <p>データは、グレーまたはrgbに変換した後、パレットに変換されます。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>いいえ </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> quantize= </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> heic </p> </td> 
   <td colname="col2"> <p>rgb </p> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/heic&gt; </span> </p> </td> 
   <td colname="col4"> <p>いいえ </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000、jpeg2000-alpha </p> </td> 
   <td> <p>rgb、グレー </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/jp2&gt; </span> </p> </td> 
   <td> <p>いいえ </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname">圧縮</span> </span> （<span class="codeph">非可逆</span>、<span class="codeph">可逆</span>） </p> <p> <span class="codeph"> qlt= </span>は、<span class="codeph">の可逆性</span>に対して無視されます。 </p> <p>WebP形式ではクロミナンスのダウンサンプリングという概念はないため、<span class="codeph"> qlt </span>の2番目の値（例：<span class="codeph"> qlt=80,1 </span>）を使用する場合、2番目の値（<span class="codeph"> 1 </span>）は無視されます。 </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg、jpg、pjpeg </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>, <span class="codeph"> pscan= </span>, <span class="codeph"> qlt= </span>, <span class="codeph"> xmpEmbed= </span> </p> <p><span class="codeph"> pscan= </span> パラメーターは、pjpeg形式にのみ適用されます。 </p> </td> 
  </tr>
  <tr valign="top"> 
   <td> <p>jpegxr、jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/vnd.ms-photo&gt; </span> </p> </td> 
   <td> <p>いいえ </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname">圧縮</span> </span> （<span class="codeph">非可逆</span>、<span class="codeph">可逆</span>） </p> <p> <span class="codeph"> qlt= </span>は、<span class="codeph">の可逆性</span>に対して無視されます。 </p> <p>WebP形式ではクロミナンスのダウンサンプリングという概念はないため、<span class="codeph"> qlt </span>の2番目の値（例：<span class="codeph"> qlt=80,1 </span>）を使用する場合、2番目の値（<span class="codeph"> 1 </span>）は無視されます。 </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> PDF </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname">圧縮</span> </span> <p> （<span class="codeph"> none|zip|jpeg </span>）, <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span>は、<span class="codeph"> <span class="varname">圧縮</span> </span>が<span class="codeph"> jpeg </span>に設定されていない限り無視されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb、グレー </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb、グレー </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>いいえ </p> <p> <p>注意：Adobe Flash Playerでは、埋め込まれたICC プロファイルは無視されます。 </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>、<span class="codeph">属性：:TrustedDomains </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname">圧縮</span> </span> <p> （<span class="codeph"> none|lzw|zip|jpeg </span>） </p> <p>'tiff'のみ；'tiff-alpha'はjpeg圧縮をサポートしていません。 </p> <p> <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span>は、<span class="varname">圧縮</span>が<span class="codeph"> jpeg </span>に設定されていない限り無視されます。 </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>webp, webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/webp&gt; </span> </p> </td> 
   <td> <p>いいえ </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname">圧縮</span> </span> （<span class="codeph">非可逆</span>、<span class="codeph">可逆</span>） </p> <p> <span class="codeph"> qlt= </span>は、<span class="codeph">の可逆性</span>に対して無視されます。 </p> <p>WebP形式ではクロミナンスのダウンサンプリングという概念はないため、<span class="codeph"> qlt </span>の2番目の値（例：<span class="codeph"> qlt=80,1 </span>）を使用する場合、2番目の値（<span class="codeph"> 1 </span>）は無視されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

リクエスト属性： `req=img` （デフォルト）または`req=mask`の場合、現在のレイヤー設定に関係なく適用されます。それ以外の場合は無視されます。

`iccProfile=`が指定されている場合、*`type`*&#x200B;は無視されます。

## 初期設定 {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`。ここで&#x200B;*`defaultType`*&#x200B;は次のように処理されます。`icc=`が指定されている場合、*`defaultType`*&#x200B;は指定されたICC プロファイルのピクセルタイプに対応します。 `icc=`が指定されていない場合、*`defaultType`*&#x200B;は`req=mask`の場合は`gray`、それ以外の場合は`rgb`です。

## 例 {#section-b93222e652df404a84c69025247f07df}

**JPEG形式の低画質の小さいプレビュー画像をリクエストする（デフォルト）:**

` http:// *` サーバー`*/myRootId/myImageId?qlt=60&wid=200`

**グレースケールに変換された同じ画像をリクエスト：**

` http:// *` サーバー`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**アルファチャンネルと高解像度のロスレス形式で同じ画像をリクエストします：**

` http:// *` サーバー`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**グレースケールのTIFF画像と同じ画像のアルファチャンネルをリクエスト：**

` http:// *` サーバー`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**デフォルトのICC プロファイルを使用して、同じ画像をcmykに変換します：**

` http:// *` サーバー`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**同じ画像を別のICC プロファイルを使用してcmykに変換し、TIFF画像にプロファイルを埋め込みます：**

` http:// *` サーバー`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**この画像をJPEG圧縮のTIF ファイルとして提供します。ピクセル形式は変換されません：**

` http:// *` サーバー`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**キーカラーの透明度とフォース カラーを白黒に変換した両色調のGIFに画像を変換します：**

` http:// *` サーバー`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

品質設定が80:**の** Lossy

` http:// *` サーバー`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

アルファ **を使用した**&#x200B;損失

` http:// *` サーバー`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

品質設定が80:**の** Lossy

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

アルファ **を使用した**&#x200B;損失

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

品質設定が80:**の** Lossy

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

アルファ **を使用した**&#x200B;損失

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## 関連項目 {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352)、[quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)、[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、[icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)、[iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)、[pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301)、[pscan](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135)。
