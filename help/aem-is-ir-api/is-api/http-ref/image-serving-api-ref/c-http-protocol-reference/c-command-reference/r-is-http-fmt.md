---
title: fmt
description: 応答画像形式。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
source-git-commit: 9ed415c5ab4444a2d404782bfd96ded3c47c26cd
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 2%

---

# fmt{#fmt}

応答画像形式。

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* - avif-alpha | avif | eps | f4m | gif-alpha | gif | 熱の | jpeg | jpeg2000-alpha | jpeg2000 | jpegxr-alpha | jpegxr | jpg | m3u8 | pdf | pjpeg | png-alpha | png | png8-alpha | png8 | swf-alpha | swf | swf3-alpha | swf3 | tif-alpha | tif | web-alpha | webp

| *`format`* | 説明 |
|---|---|
| `avif-alpha` | アルファチャンネル付きの非可逆および非可逆 AVIF。 |
| `avif` | 可逆および可逆 AVIF。 |
| `eps` | 非圧縮バイナリ Encapsulated PostScript。 |
| `f4m` | Flashストリーミングサーバーのマニフェスト形式。 |
| `gif-alpha` | 2 ～ 255 色とキーカラーの透明度を併せ持つGIF。 |
| `gif` | 2～256 色のGIF。 |
| `heic` | ロスレス HEIC。 この形式がサポートされていない場合は、デフォルトでブラウザーからダウンロードされます。 |
| `jpeg` | 非可逆JPEG。 |
| `jpeg2000-alpha` | アルファチャンネル付きの非可逆JPEG2000。 |
| `jpeg2000` | 非可逆および非可逆JPEG2000。 |
| `jpegxr-alpha` | アルファチャンネル付きのロスレスJPEGXR。 |
| `jpegxr` | 可逆および可逆JPEGXR。 |
| `jpg` | 非可逆JPG。 |
| `m3u8` | Appleストリーミングサーバのマニフェスト形式。 |
| `pdf` | 画像が埋め込まれましたPDF。 |
| `pjpeg` | プログレッシブJPEG。 |
| `png-alpha` | アルファチャンネル付きの 24 ビット可逆 PNG。 |
| `png` | 24 ビット可逆 PNG。 |
| `png8-alpha` | アルファチャンネル付きの 8 ビット可逆 PNG。 |
| `png8` | 8 ビット可逆 PNG。 |
| `swf-alpha` | 非可逆JPEGと、AdobeAS2 swf ファイルに埋め込まれたデフレート圧縮マスク。 |
| `swf` | 非可逆JPEGは、AdobeAS2 swf ファイルに埋め込まれています。 |
| `swf3-alpha` | 非可逆JPEGと、AdobeAS3 swf ファイルに埋め込まれたデフレート圧縮マスク。 **注意：** swf および swf-alpha 形式は、ActionScript2 アプリケーション (Flash Player8 以前 ) に最適です。 ActionScript3 アプリケーション (Flash Player9 以降 ) では、 swf3 および swf3-alpha 形式を使用することをお勧めします。 |
| `swf3` | 非可逆JPEGは、AdobeAS3 swf ファイルに埋め込まれています。 |
| `tif-alpha` | TIFF（アルファチャンネル） |
| `tif` | TIFF。 |
| `webp-alpha` | アルファチャンネル付きの非可逆 WebP。 |
| `webp` | 非可逆および非可逆 WebP。 |

| *`pixelType`* - rgb | グレー | cmyk |
| *`pixelType`* | 説明 |
|---|---|
| `cmyk` | CMYK 画像データを返します。 |
| `gray` | グレースケールの画像データを返します。 |
| `rgb` | RGB画像データを返す。 |

| *`compression`* - jpeg | 可逆 | ロスレス | lzw | 除外 | zip |
| *`compression`* | 説明 |
|---|---|
| `jpeg` | JPEG圧縮（非可逆）。 |
| `lossy` | WebP、JPEG2000、およびJPEGXR 圧縮（非可逆）。 |
| `lossless` | WebP、JPEG2000、およびJPEGXR 圧縮（ロスレス）。 |
| `lzw` | LZW(Lempel-Ziv-Welch) 圧縮（ロスレス）。 |
| `none` | 非圧縮。 |
| `zip` | 「デフレート」圧縮（ロスレス）。 |

* *`format`* クライアントに送信する画像データの画像エンコーディング形式と、HTTP 応答ヘッダーに対応する応答 MIME タイプを指定します。
* *`pixelType`* を使用すると、 `icc=` が指定されていません。

  次に対応するデフォルトのカラープロファイル： *`pixelType`* が適用されます。 カラーマネジメントが無効な場合、ネイティブ変換が適用されます。 *`pixelType`* 次の場合は無視されます： `icc=` が指定され、出力ピクセルタイプを決定します。

* *`compression`* 次の場合にのみ許可されます。 `tif`, `tif-alpha`, `pdf`, `webp`, `webp-alpha`, `jpeg2000`, `jpeg2000-alpha`, `jpegxr`または `jpegxr-alpha` が *`format`*. これらの画像形式でサポートされる圧縮オプションについては、次の表を参照してください。

以下を使用できます。 `qlt=` を使用して、JPEG、JPEG圧縮を使用したTIFF、JPEG圧縮を使用したPDF、SWFの各形式に対してJPEGエンコーディングオプションを設定します。 WebP、JPEG2000、JPEGXR も使用 `qlt=` しかし、値の結果、形式が異なれば、品質も異なります。 用途 `quantize=` if `fmt=gif` または `fmt=gif-alpha`. 詳しくは、コマンドの説明を参照してください。 その他の形式には、設定可能なオプションはありません。

ピクセルあたり 8 ビットのコンポーネントが、すべての *`formats`* および *`pixelTypes`* (GIFの場合は 8 ビット/ピクセル )。

次の表に、*の有効な組み合わせを示します。`format`*および *`pixelType`*、対応する HTTP 応答 MIME タイプ、ICC プロファイルを埋め込めるかどうか ( [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)) や、適用できる形式固有のオプションを示します。

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> 形式</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b> 応答の MIME タイプ</b> </th> 
   <th class="entry"> <b>ICC プロファイルを埋め込む</b> </th> 
   <th class="entry"> <b> オプション</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>, <span class="codeph"> pscan= </span>, <span class="codeph"> qlt= </span>, <span class="codeph"> xmpEmbed= </span> </p> <p>The <span class="codeph"> pscan= </span> パラメーターは pjpeg 形式にのみ適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb、グレー </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 圧縮 </span> </span> <p> ( <span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>「tiff」のみ。「tiff-alpha」は jpeg 圧縮をサポートしていません。 </p> <p> <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> 次の場合を除き無視されます： <span class="varname"> 圧縮 </span> が <span class="codeph"> jpeg </span>. </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf, swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb、グレー </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>いいえ </p> <p> <p>注意：AdobeFlash Playerは、埋め込まれた ICC プロファイルを無視します。 </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>, <span class="codeph"> attribute::TrustedDomains </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> PDF </p> </td> 
   <td colname="col2"> <p>rgb、グレー、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 圧縮 </span> </span> <p> ( <span class="codeph"> none|zip|jpeg </span>), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> 次の場合を除き無視されます： <span class="codeph"> <span class="varname"> 圧縮 </span> </span> が <span class="codeph"> jpeg </span>. </p> </td> 
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
   <td colname="col2"> <p>rgb、グレー </p> <p>グレーまたは rgb に変換した後、データがパレットに変換されます。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>いいえ </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> quantize= </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>webp, webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/webp&gt; </span> </p> </td> 
   <td> <p>いいえ </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> 圧縮 </span> </span> ( <span class="codeph"> 可逆 </span>, <span class="codeph"> ロスレス </span>) </p> <p> <span class="codeph"> qlt= </span> 次の値は無視されます： <span class="codeph"> ロスレス </span>. </p> <p>WebP 形式でのクロミナンスダウンサンプリングの概念がないので、 <span class="codeph"> qlt </span> ( 例： <span class="codeph"> qlt=80,1 </span>)2 番目の値 ( <span class="codeph"> 1 </span>) は無視されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000, jpeg2000-alpha </p> </td> 
   <td> <p>rgb、グレー </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/jp2&gt; </span> </p> </td> 
   <td> <p>いいえ </p> </td> 
   <td> <p>上記と同じ。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/vnd.ms-photo&gt; </span> </p> </td> 
   <td> <p>いいえ </p> </td> 
   <td> <p>上記と同じ。 </p> </td> 
  </tr>
  <tr valign="top"> 
   <td> <p> avif, avif-alpha </p> </td> 
   <td> <p>rgb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image/avif&gt; </span> </p> </td> 
   <td> <p>いいえ </p> </td> 
   <td> <p>上記と同じ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

要求属性。 次の場合、現在の画層設定に関係なく適用されます。 `req=img` （デフォルト）または `req=mask`；それ以外の場合は無視されます。

*`type`* 次の場合は無視されます： `iccProfile=` が指定されている。

## 初期設定 {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`( ここで *`defaultType`* は次のように処理されます。 `icc=` が指定されている場合、 *`defaultType`* は、指定した ICC プロファイルのピクセルタイプに対応します。 次の場合 `icc=` が指定されていません。 *`defaultType`* 次に該当 `gray` if `req=mask`、それ以外の場合は `rgb`.

## 例 {#section-b93222e652df404a84c69025247f07df}

**画質の低い小さなプレビュー画像をJPEG形式（デフォルト）で要求します。**

` http:// *`server`*/myRootId/myImageId?qlt=60&wid=200`

**グレースケールに変換された同じ画像をリクエストします。**

` http:// *`server`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**アルファチャンネルと高解像度を使用して、同じ画像を損失のない形式で要求します。**

` http:// *`server`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**グレースケールの画像と同じ画像に対して、アルファチャンネルをTIFFします。**

` http:// *`server`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**初期設定の ICC プロファイルを使用して、同じ画像を cmyk に変換します。**

` http:// *`server`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**同じ画像を別の ICC プロファイルを使用して cmyk に変換し、そのプロファイルをTIFF画像に埋め込みます。**

` http:// *`server`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**この画像を、ピクセルタイプ変換を行わずに、JPEG圧縮を使用して TIF ファイルとして配信します。**

` http:// *`server`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**画像をキーカラー透明度でバイトーンGIFに変換し、カラーを白黒に強制的に変換します。**

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**品質設定が 80 の非可逆**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**アルファ付きロスレス：**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**品質設定が 80 の非可逆**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**アルファ付きロスレス：**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**品質設定が 80 の非可逆**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**アルファ付きロスレス：**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## 関連項目 {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301), [pscan](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135).
