---
description: 画像変換ユーティリティ
seo-description: 画像変換ユーティリティ
seo-title: ic
solution: Experience Manager
title: ic
topic: Scene7 Image Serving - Image Rendering API
uuid: 08fabcc9-d0b5-4136-81fc-ac896c341e1d
translation-type: tm+mt
source-git-commit: e0f8153b038446180ddad313e591828223ed31e9

---


# ic {#ic}

画像変換ユーティリティ

`ic` は、画像ファイルを最適化されたピラミッドTIFF形式(PTIFF)に変換するコマンドラインツールです。 画像サービングでは変換せずに画像を処理できますが、512 x 512ピクセルを超えるすべての画像をPTIFFに変換することをお勧めします。 この変換により、最適なサーバのパフォーマンスとリソース使用率を確保し、応答時間を最小限に抑えます。

写真コンテンツを含むPTIFFファイルは、JPEGでエンコード(指定 `-jpegcompress`)することをお勧めします。 コンピュータ生成コンテンツは、可逆圧縮(または `-deflatecompress` )の利点が `-lzwcompress`あります。 色変換またはピクセルタイプ変換が必要な場合を除き、画質の低下を防ぐために、JPEGソース画像データはデコードせずにPTIFFに転送されます。 この場合、指定した圧縮オプションは、低解像度の角錐レベルにのみ適用されます。

大きな画像を変換しない場合は、使用するメモリ量を制御するパラメータを設定する必要はありません。 ただし、メモリが多い場合は、以 `ic` 下の設定を使用して `-maxmem` メモリを増やします。 必要なメモリ量を計算する目安として、イメージの幅にイメージの高さにチャネル数を掛けるのが良い方法です。 例えば、アルファが3倍のRGB画像の場合は4です。 さらに、チャネルが8ではなく16ビット/コンポーネントの場合は、最終的な結果が2倍になります。

## 使用方法 {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]` *`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]` *`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]` *`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> オプシ <span class="varname"><i>ョン</i></span></span> </p> </td> 
   <td colname="col2"> <p>コマンドオプション（以下を参照）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> sourceFile <i></i></span></span> </p> </td> 
   <td colname="col2"> <p>単一の入力画像ファイル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span></span> </p> </td> 
   <td colname="col2"> <p>単一の出力PTIFFファイル（SourceDirectoryと共に使用する場合は無効）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span></span> </p> </td> 
   <td colname="col2"> <p>入力画像を含むフォルダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span></span> </p> </td> 
   <td colname="col2"> <p>出力PTIFFファイルの書き込み先フォルダー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-36a2dcfa39824d29b69547c432366219}

0（成功した場合） エラーが発生した場合は、ゼロ以外の値が返され、エラーの詳細がに送信されま `stderr`す。

## オプション {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -未圧縮 </span> </p> </td> 
   <td colname="col2"> <p>出力画像は圧縮しないでください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress </span> </p> </td> 
   <td colname="col2"> <p>deflate(zip)圧縮（デフォルト）を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress </span> </p> </td> 
   <td colname="col2"> <p>Lempel-Ziv-Welch(LZW)圧縮を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress </span> </p> </td> 
   <td colname="col2"> <p>JPEGエンコーディングを使用します。 sourceFileにアルファデ <span class="codeph"> ータが含ま <span class="varname"> れる場合は </span></span> 無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality &lt; <span class="varname"> quality </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>JPEG画質(0 ～ 100、初期設定は95)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplecrominance </span> </p> </td> 
   <td colname="col2"> <p>JPEGのクロマダウンサンプリングを無効にします（カラーテキストとグラフィックの品質が向上します）。 これは、CMYKまたはグレースケールの出力画像には影響しません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm &lt; <span class="varname"> amount </span>&gt; &lt; <span class="varname"> radius </span>&gt; &lt; <span class="varname"> threshold </span>&gt; &lt; <span class="varname"></span>monochrome&gt; </span> </p> </td> 
   <td colname="col2"> <p>アンシャープマスクをサブサンプルピラミッドレベルに適用します。 詳し <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> くは、op_usm=を参 </a> 照してください。 （最大解像度の画像には適用されません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath </span> </p> </td> 
   <td colname="col2"> <p>ソースファイル内にクリップパスが存在する場合は、そのパスを使用して、関連するアルファデータを作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi &lt; <span class="varname"> dpi </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>destFileの印刷解像度(dpi) <span class="codeph"><span class="varname"></span></span>;指定しなかった場合、 <span class="codeph"> srcFileの印刷解像 </span> 度がdestFileにコピ <span class="codeph"> ーさ <span class="varname"> れま </span></span>す。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocrop &lt; <span class="varname"> corner </span>&gt; &lt; <span class="varname"> mode&gt; &lt; </span>tolerance <span class="varname"> &lt; </span>info <span class="varname"></span>file&gt; </span> </p> </td> 
   <td colname="col2"> <p>切り抜き長方形を計算し、背景色を最小限に抑えます。 自動切り抜きアルゴリズムによって画像全体が切り抜かれる場合、切り抜き情報は出力されません。 </p> <p>画像を変換せずに切り抜き長方形を計算するには、-convertを指定せず <span class="codeph"> に、 </span> destFileを指定 <span class="codeph"> せずに —autocropを指 </span><span class="codeph"><span class="varname"> 定します。</span> </span></p>

<p><i><b>角</b></i> - ul| ur| ll| lr </p>
   <p> シードポイントを使用する画像の隅を指定します。 modeが1の場合は無視されます。</p>
   <p><i><b>mode</b></i> - 0| 1</p>
   <p>0に設定すると、指定した角のピクセルの色に基づいて切り抜かれます。アルファデータがソース画像に関連付けられている場合、乗算済みのカラーデータに対して機能します。</p>
   <p>アルファデータに基づいて切り抜くには、1に設定します。cornerは無視され、0が常にシード値です。ソース画像にアルファデータが関連付けられていない場合、切り抜きは適用されません。</p> 
   <p><i><b>許容値</b></i> — マッチ許容値。 0.0 ～ 1.0の実数です。ピクセルコンポーネントの値を一致させるための許容値を指定します。 完全一致の場合は0に設定します。</p>
   <p><i><b>infoFile</b></i> — 切り抜き情報データの書き込み先となるXML出力ファイルのパスと名前。</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData </span> </p> </td> 
   <td colname="col2"> <p>XMPメタデータがある場合は、それを <span class="codeph"> sourceFileから <span class="varname"></span> dest変 </span> 更な <span class="codeph"> しで <span class="varname"> Fileにコ </span></span> ピーします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile </span> </p> </td> 
   <td colname="col2"> <p> 使用可能な場合は、ICCカラープロファイルを <span class="codeph"> destFileに埋 <span class="varname"> め込みます(デフ </span></span>ォルトでは、プロファイルは埋め込まれません)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ICCプロファイルファイルのパスと名前。 sourceFileのカラースペースを定義し、そ <span class="codeph"> のピクセ <span class="varname"> ルタイプと一 </span> 致さ </span> せる必要があります。 プロファイルがsourceFileに埋め込まれていない場合にのみ指定する必要があります。これは、埋め込ま <span class="codeph"> れたプロファ <span class="varname"></span></span>イルを上書きするためです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ICCプロファイルファイルのパスと名前。 destFileのピクセルタイプとカラースペースを <span class="codeph"> 定義 <span class="varname"> しま </span></span>す。 sourceFileに埋め込みプロファイルが含まれている場合、または <span class="codeph"> -imageprofile <span class="varname"> が指定されている場合、ICはこ </span> のプロファイルに変 </span><span class="codeph"></span> 換されます。この場合、ICはこのプロファイルにも変換されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptical </span> </p> </td> 
   <td colname="col2"> <p>カラースペース変換の知覚的なレンダリングインテント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric </span> </p> </td> 
   <td colname="col2"> <p> カラースペース変換の相対的な色域を維持レンダリングインテント（初期設定）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimetric </span> </p> </td> 
   <td colname="col2"> <p>カラースペース変換の絶対的な色域を維持レンダリングインテント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation </span> </p> </td> 
   <td colname="col2"> <p>彩度レンダリングインテントを使用して、カラースペースの変換を行います。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation </span> </p> </td> 
   <td colname="col2"> <p>特定の色変換のブラックポイント補正の無効化 </p> <p>デフォルトで有効です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8 </span> </p> </td> 
   <td colname="col2"> <p>色変換時にディザリング（エラー拡散）を無効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintainpixeltype </span> </p> </td> 
   <td colname="col2"> <p> CMYKからRGBへの自動変換を無効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress </span> </p> </td> 
   <td colname="col2"> <p>JPEG入力画像のデコードと再エンコードを強制的に実行します。 </p> <p> <b>注意：</b> このオプションを適用すると、画質が低下する場合があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2 </span> </p> </td> 
   <td colname="col2"> <p>標準品質（バイリニア）のリサンプリングフィルタを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8 </span> </p> </td> 
   <td colname="col2"> <p>より高い品質（ランチョス窓）の再サンプリングフィルタ（デフォルト）を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix </span> </p> </td> 
   <td colname="col2"> <p>より高品質な(FlashPix)リサンプリングフィルタを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp </span> </p> </td> 
   <td colname="col2"> <p>Photoshopスタイルの8x8バイキュービックシャープフィルターを使用したダウンサンプル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">  — ヌサジ </span> </p> </td> 
   <td colname="col2"> <p> 最初のオプションとして指定した場合、無効なオプションが見つかった場合に、使用状況情報の出力を抑制します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -上書き </span> </p> </td> 
   <td colname="col2"> <p>既存の <span class="codeph"> destFileを上書きで <span class="varname"> きます </span></span>。 デフォルトでは、上書きを防ぐために、ファイル名に数値のサフィックスが追加されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphidden </span> </p> </td> 
   <td colname="col2"> <p>非表示のソースファイルを無視します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror </span> </p> </td> 
   <td colname="col2"> <p>エラーが発生した場合は処理を停止しないでください。 複数のファイルを処理する場合にのみ有効です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ログファイルのパスと名前(デフォルトは <span class="codeph"> stdout </span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel &lt; <span class="varname"> level </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ログレベル。 </p> 
   <p>&lt; 0 — ログが無効です。</p>
   <p>0 — 処理するファイルを一覧表示します。</p>
   <p>1 — 不要なファイルのレポートを追加します。</p>
   <p>2 — 進行状況レポートを追加します。</p>
   <p>3 — 検出されたすべてのファイルにレポートを追加します。</p>
   <p>4 — 進行状況レポートをファイルレベルで追加します。</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend </span> </p> </td> 
   <td colname="col2"> <p>ログファイルに追加（デフォルト） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend </span> </p> </td> 
   <td colname="col2"> <p>ログファイルを上書きします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogressmsec &lt; <span class="varname"> msec </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>loglevel 2以降のログ間隔（ミリ秒）（デフォルトは3000）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem &lt;バ <span class="varname"> イト </span>数&gt; </span> </p> </td> 
   <td colname="col2"> <p>メモリ使用量の制限。 10 MB以上にする必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent &lt; <span class="varname"> percent </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>メモリ使用量の制限。 初期設定は、物理メモリの25%です。 maxmemもmaxmempercentも明示的に設定さ <span class="codeph"> れていない場 </span><span class="codeph"></span> 合は、maxmempercentのデフォルト値が使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -バージョン </span> </p> </td> 
   <td colname="col2"> <p> このユーティリティのバージョン情報を返します。 その他のオプションは使用しないで指定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## サポートされる入力画像形式 {#section-ab13d941d6724e65b9f84b62d949d31c}

次の表に、ICでサポートされている画像ファイル形式と形式オプションを示します。

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> 形式</b> </p> </th> 
   <th class="entry"> <p> <b> Pixel Type</b> Bits <b> /Chan</b> </p> </th> 
   <th class="entry"> <p> <b> ビット/チャン</b> </p> </th> 
   <th class="entry"> <p> <b> 圧縮</b> </p> </th> 
   <th class="entry"> <p> <b> 説明</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> （Windowsビットマップ） </p> </td> 
   <td> <p> RGB|インデックス付き </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> 非圧縮| RLE </p> </td> 
   <td> <p> 5/6ビット/チャネルは、16ビットRGB（5-5-5および5-6-5ビット/チャネル）のサポートを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (Encapsulated Postscript) </p> </td> 
   <td> <p> CMYK| RGB| gray </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII| ASCII85|バイナリ| JPEG </p> </td> 
   <td> <p> Photoshopで生成されたEPSファイルのみがサポートされます。 </p> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> <p> CompuServe </p> <b>GIF</b> </td> 
   <td> <p> インデックス </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> LZW </p> </td> 
   <td> <p> 存在する場合、パレットの透明度の値がアルファに変換されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG</b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMYK| RGB| gray </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK| CMYKA| RGB| RGBA| gray| grayA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 非圧縮|圧縮 </p> </td> 
   <td> <p> 結合された画像のみ；レイヤーと余分なチャンネルは無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RLE </p> </td> 
   <td> <p> ビットマップデータのみ、ベクトルデータは無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB| RGBA| gray| grayA|インデックス付き </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> 圧縮 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK| CMYKA| RGB| RGBA| gray| grayA|インデックス付き </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 非圧縮| ZIP| LZW| JPEG| CCITT RLE| CCITT G3| CCITT G4|パッケージ </p> </td> 
   <td> <p> 最初に関連付けられたアルファチャンネルを除き、余分なチャンネルは無視されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

埋め込まれたICCプロファイルは、EPS、JPG、PSD、PNGおよびTIFFファイルで認識されます。

埋め込みパスとXMPメタデータは、EPS、JPG、PSDおよびTIFFファイルで認識されます。

## 例 {#section-3c1986b30315431989bd76b1ee5bef6d}

1つの画像を最高の画質で変換し、同じフォルダーに保つ：

`ic -convert src/myFile.png src/myFile.tif`

すべての画像をJPEGでエンコ *`srcFolder`* ードされたピラミッドTIFFに変換し、次の場所に配置しま *`destFolder`*&#x200B;す。

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

ですべての画像を変換しま *`srcFolder`*&#x200B;す。 JPGファイルのエンコードされた画像データは、これらの画像の残りの画像角錐の部分に対して、また、すべての非JPG入力ファイルの出力画像全体に対して、フル解像度レベルの損失なしLZW圧縮に使用されます。 ピクセルタイプ、埋め込みカラープロファイル、XMPメタデータなど。 が維持される。

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
