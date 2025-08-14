---
title: fmt
description: 応答画像の形式。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 2%

---

# fmt{#fmt}

応答画像の形式。

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* - avif-α | avif | eps | f4m | gif アルファ | gif | ハイク | jpeg | jpeg2000 アルファ | jpeg2000 | jpegxr-alpha | jpegxr | jpg | m3u8 | pdf | pjpeg | png-alpha | png | png8 アルファ | png8 | swf-alpha | swf | swf3-α | swf3 | tif アルファ | tif | web アルファ | webp

| *`format`* | 説明 |
|---|---|
| `avif-alpha` | アルファチャンネル付きの非可逆および非可逆 AVIF。 |
| `avif` | 非可逆および非可逆 AVIF。 |
| `eps` | 非圧縮バイナリでカプセル化されたPostScript。 |
| `f4m` | Flash ストリーミングサーバーマニフェスト形式。 |
| `gif-alpha` | 2～255 色のGIFにキーカラーの透明度を追加。 |
| `gif` | GIF（2～256 色） |
| `heic` | 可逆ハイク。 この形式がサポートされていない場合、デフォルトでブラウザーからダウンロードされます。 |
| `jpeg` | 非可逆JPEG。 |
| `jpeg2000-alpha` | アルファチャンネル付き非可逆式JPEG 2000。 |
| `jpeg2000` | 非可逆および非可逆JPEG 2000。 |
| `jpegxr-alpha` | アルファチャンネル付き非可逆および非可逆JPEG XR。 |
| `jpegxr` | 非可逆および非可逆JPEG XR。 |
| `jpg` | 非可逆JPG。 |
| `m3u8` | Apple Streaming Server マニフェスト形式。 |
| `pdf` | PDFに埋め込まれた画像。 |
| `pjpeg` | プログレッシブ JPEG。 |
| `png-alpha` | アルファチャンネル付き 24 ビットの可逆圧縮 PNG |
| `png` | 24 ビットロスレス PNG。 |
| `png8-alpha` | アルファチャンネル付き 8 ビットの可逆圧縮 PNG |
| `png8` | 8 ビットロスレス PNG |
| `swf-alpha` | 非可逆JPEGと、Adobe AS2 swf ファイルに埋め込まれた圧縮マスク。 |
| `swf` | Adobe AS2 swf ファイルに埋め込まれた非可逆JPEG。 |
| `swf3-alpha` | 非可逆JPEGと、Adobe AS3 swf ファイルに埋め込まれた圧縮マスク。 **注意：** swf および swf-alpha 形式は、ActionScript 2 アプリケーション（Flash Player 8 以前）で最もよく使用されます。 swf3 および swf3-alpha の形式は、ActionScript3 アプリケーション（Flash Player 9 以降）での使用をお勧めします。 |
| `swf3` | Adobe AS3 swf ファイルに埋め込まれた非可逆JPEG。 |
| `tif-alpha` | アルファチャンネルのTIFF |
| `tif` | TIFF。 |
| `webp-alpha` | アルファチャンネル付きの可逆および可逆性 WebP。 |
| `webp` | 非可逆および非可逆 WebP |

*`pixelType`* - rgb |灰色 | cmyk

| *`pixelType`* | 説明 |
|---|---|
| `cmyk` | CMYK 画像データを返します。 |
| `gray` | グレースケールの画像データを返します。 |
| `rgb` | RGBの画像データを返します。 |

*`compression`* - jpeg |非可逆 |可逆 | lzw |なし |郵便番号

| *`compression`* | 説明 |
|---|---|
| `jpeg` | JPEG圧縮（非可逆）。 |
| `lossy` | JPEG 2000、JPEG XR 圧縮（非可逆）、および WebP |
| `lossless` | HEIC、JPEG 2000、JPEG XR 圧縮（可逆圧縮）、WebP |
| `lzw` | LZW （Lempel-Ziv-Welch）圧縮（ロスレス） |
| `none` | 非圧縮。 |
| `zip` | 「圧縮を圧縮する」（可逆圧縮） |

* クライアント *`format`* 送信する画像データの画像エンコーディング形式と、HTTP 応答ヘッダーに対応する応答 MIME タイプを指定します。
* *`pixelType`* は、`icc=` が指定されていない場合に出力カラースペース変換を行うために使用できます。

  *`pixelType`* に対応するデフォルトのカラープロファイルが適用されます。 カラーマネジメントが無効の場合、ネイティブ変換が適用されます。 *`pixelType`* が指定されている場合、`icc=` は無視されます。これにより出力ピクセルのタイプが決まります。

* *`compression`* は、`tif`、`tif-alpha`、`pdf`、`webp`、`webp-alpha`、`jpeg2000`、`jpeg2000-alpha`、`jpegxr` または `jpegxr-alpha` が *`format`* として指定されている場合にのみ許可されます。 これらの画像形式でサポートされる圧縮オプションについては、次の表を参照してください。

`qlt=` を使用して、JPEG、JPEG圧縮のTIFF、JPEG圧縮のPDFおよびSWFの各形式に対してJPEG エンコーディングオプションを設定できます。 WebP、JPEG 2000、JPEG XR でも `qlt=` を使用しますが、値の結果はフォーマットによって異なります。 `quantize=` または `fmt=gif` の場合は `fmt=gif-alpha` を使用します。 詳細は、コマンドの説明を参照してください。 その他の形式には、設定可能なオプションはありません。

すべての *`formats`* および *`pixelTypes`* に対して、1 ピクセルあたり 8 ビットのコンポーネントが返されます（GIFの場合は 1 ピクセルあたり 8 ビット）。

次の表に、*`format`*と *`pixelType`* の有効な組み合わせ、対応する HTTP 応答の MIME タイプ、ICC プロファイルを埋め込むことができるかどうか（[iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e) を参照）、適用できる形式固有のオプションを示します。

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> 形式 </i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> 応答 <b>MIME タイプ </b> </th> 
   <th class="entry"> <b>ICC プロファイルの埋め込み </b> </th> 
   <th class="entry"> <b> Options</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> avif、avif-α </p> </td> 
   <td> <p>rgb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image/avif&gt; </span> </p> </td> 
   <td> <p>いいえ </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> 圧縮 </span> </span> （<span class="codeph"> 非可逆 </span>、<span class="codeph"> 非可逆 </span>） </p> <p> <span class="codeph"> qlt= </span> は、<span class="codeph"> の可逆 </span> では無視されます。 </p> <p>WebP 形式ではクロミナンスのダウンサンプリングの概念がないため、2 番目の値を <span class="codeph"> qlt </span> で使用する場合（例：<span class="codeph"> qlt=80,1 </span>）、2 番目の値（<span class="codeph"> 1 </span>）は無視されます。 </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb, グレー，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif アルファ </p> </td> 
   <td colname="col2"> <p>rgb、グレー </p> <p>データは、グレーまたは rgb に変換された後、パレットに変換されます。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>いいえ </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> quantize= </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> ヒック </p> </td> 
   <td colname="col2"> <p>rgb </p> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/heic&gt; </span> </p> </td> 
   <td colname="col4"> <p>いいえ </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000、jpeg2000 アルファ </p> </td> 
   <td> <p>rgb、グレー </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/jp2&gt; </span> </p> </td> 
   <td> <p>いいえ </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> 圧縮 </span> </span> （<span class="codeph"> 非可逆 </span>、<span class="codeph"> 非可逆 </span>） </p> <p> <span class="codeph"> qlt= </span> は、<span class="codeph"> の可逆 </span> では無視されます。 </p> <p>WebP 形式ではクロミナンスのダウンサンプリングの概念がないため、2 番目の値を <span class="codeph"> qlt </span> で使用する場合（例：<span class="codeph"> qlt=80,1 </span>）、2 番目の値（<span class="codeph"> 1 </span>）は無視されます。 </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rgb, グレー，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>、<span class="codeph"> pscan= </span>、<span class="codeph"> qlt= </span>、<span class="codeph"> xmpEmbed= </span> </p> <p><span class="codeph"> pscan= </span> パラメーターは、pjpeg 形式にのみ適用されます。 </p> </td> 
  </tr>
  <tr valign="top"> 
   <td> <p>jpegxr、jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/vnd.ms-photo&gt; </span> </p> </td> 
   <td> <p>いいえ </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> 圧縮 </span> </span> （<span class="codeph"> 非可逆 </span>、<span class="codeph"> 非可逆 </span>） </p> <p> <span class="codeph"> qlt= </span> は、<span class="codeph"> の可逆 </span> では無視されます。 </p> <p>WebP 形式ではクロミナンスのダウンサンプリングの概念がないため、2 番目の値を <span class="codeph"> qlt </span> で使用する場合（例：<span class="codeph"> qlt=80,1 </span>）、2 番目の値（<span class="codeph"> 1 </span>）は無視されます。 </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> PDF </p> </td> 
   <td colname="col2"> <p>rgb, グレー，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 圧縮 </span> </span> <p> （<span class="codeph"> none|zip|jpeg </span>）、<span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> は、<span class="codeph"> 圧縮 <span class="varname"> </span> が jpeg </span><span class="codeph"> 設定されていない限り、無視 </span> れます。 </p> </td> 
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
   <td colname="col4"> <p>いいえ </p> <p> <p>メモ：Adobe Flash Player は、埋め込まれた ICC プロファイルを無視します。 </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>、<span class="codeph"> 属性：:TrustedDomains </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> tif、tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, グレー，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>はい </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 圧縮 </span> </span> <p> （<span class="codeph"> none|lzw|zip|jpeg </span>） </p> <p>「tiff」のみ。「tiff-alpha」は jpeg 圧縮をサポートしません。 </p> <p> <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> は、圧縮 <span class="varname"> が jpeg </span><span class="codeph"> 設定されていない限り無視 </span> れます。 </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>webp、webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/webp&gt; </span> </p> </td> 
   <td> <p>いいえ </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> 圧縮 </span> </span> （<span class="codeph"> 非可逆 </span>、<span class="codeph"> 非可逆 </span>） </p> <p> <span class="codeph"> qlt= </span> は、<span class="codeph"> の可逆 </span> では無視されます。 </p> <p>WebP 形式ではクロミナンスのダウンサンプリングの概念がないため、2 番目の値を <span class="codeph"> qlt </span> で使用する場合（例：<span class="codeph"> qlt=80,1 </span>）、2 番目の値（<span class="codeph"> 1 </span>）は無視されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

リクエスト属性。 `req=img` （デフォルト）または `req=mask` の場合は、現在のレイヤー設定に関係なく適用されます。それ以外の場合は無視されます。

*`type`* が指定されている場合、`iccProfile=` は無視されます。

## 初期設定 {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`、*`defaultType`* は次のように処理されます。`icc=` が指定されている場合、*`defaultType`* は指定された ICC プロファイルのピクセルタイプに対応します。 `icc=` が指定されていない場合、*`defaultType`* は `gray` の場合は `req=mask`、それ以外の場合は `rgb` です。

## 例 {#section-b93222e652df404a84c69025247f07df}

**JPEG形式の小さい低画質のプレビュー画像をリクエスト（デフォルト）:**

` http:// *` サーバー `*/myRootId/myImageId?qlt=60&wid=200`

**グレースケールに変換された同じ画像を要求：**

` http:// *` サーバー `*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**同じ画像を、アルファチャネルを使用した損失のない形式で、高解像度でリクエストする：**

` http:// *` サーバー `*/myRootId/myImageId?fmt=png-alpha&wid=300`

**グレースケールのTIFF画像と同じ画像のアルファチャンネルをリクエストする：**

` http:// *` サーバー `*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**デフォルトの ICC プロファイルを使用して、同じ画像を cmyk に変換します：**

` http:// *` サーバー `*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**別の ICC プロファイルを使用して同じ画像を cmyk に変換し、そのプロファイルをTIFF画像に埋め込みます。**

` http:// *` サーバー `*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**ピクセルタイプ変換を行わずに、JPEG圧縮を使用してこの画像を TIF ファイルとして配信する：**

` http:// *` サーバー `*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**キーカラーの透明度を持つバイトーンのGIFに画像を変換し、カラーを白黒に強制：**

` http:// *` サーバー `*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**非可逆（品質設定が 80:**）

` http:// *` サーバー `*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**アルファ付きロスレス：**

` http:// *` サーバー `*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**非可逆（品質設定が 80:**）

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**アルファ付きロスレス：**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**非可逆（品質設定が 80:**）

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**アルファ付きロスレス：**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## 関連項目 {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352)、[quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)、[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、[icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)、[iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)、[pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301)、[pscan](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135)。
