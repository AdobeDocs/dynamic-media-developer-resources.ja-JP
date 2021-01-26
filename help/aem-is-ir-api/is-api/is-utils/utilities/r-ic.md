---
description: 画像変換ユーティリティ。
seo-description: 画像変換ユーティリティ。
seo-title: ic
solution: Experience Manager
title: ic
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 08fabcc9-d0b5-4136-81fc-ac896c341e1d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '1208'
ht-degree: 2%

---


# ic {#ic}

画像変換ユーティリティ。

`ic` は、画像ファイルを最適化されたピラミッドTIFF形式(PTIFF)に変換するコマンドラインツールです。画像サービングでは変換なしで画像を処理できますが、512 x 512ピクセルを超えるすべての画像をPTIFFに変換することをお勧めします。 この変換により、最適なサーバーパフォーマンスとリソース使用率が確保され、応答時間が最小限に抑えられます。

写真コンテンツを含むPTIFFファイルは、JPEGでエンコードすることをお勧めします（`-jpegcompress`を指定します）。 コンピュータ生成コンテンツは、可逆圧縮（`-deflatecompress`または`-lzwcompress`）の利点があります。 色変換またはピクセルタイプ変換が必要な場合を除き、画質劣化を防ぐために、JPEGソース画像データはデコードせずにPTIFFに転送されます。 この場合、指定した圧縮オプションは低解像度ピラミッドレベルにのみ適用されます。

大きい画像を変換しない場合は、使用するメモリ量を制御するパラメータを設定する必要はありません。 ただし、メモリを`ic`増やす場合は、下記の`-maxmem`設定を使用してください。 必要なメモリ量を計算する目安として、画像の幅にチャネルの高さに画像の数を掛けた値を掛けるのが適切です。 例えば、アルファに3を掛けたRGB画像の場合は4です。 さらに、チャネルが8重複ではなく16ビット/コンポーネントの場合は、最終的な結果になります。

## 使用方法 {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]`*`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]`*`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]`*`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>options</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>コマンドオプション（下記を参照）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> <i>sourceFile</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>単一の入力画像ファイル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span> </span> </p> </td> 
   <td colname="col2"> <p>単一出力PTIFFファイル（SourceDirectoryと共に使用する場合は無効） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>入力画像が格納されているフォルダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>出力PTIFFファイルの書き込み先フォルダー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section-36a2dcfa39824d29b69547c432366219}を返す

成功した場合は0。 エラーが発生した場合は、ゼロ以外の値が返され、エラーの詳細が`stderr`に送られます。

## オプション {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -未圧縮 </span> </p> </td> 
   <td colname="col2"> <p>出力画像は圧縮しないでください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress  </span> </p> </td> 
   <td colname="col2"> <p>deflate(zip)圧縮（デフォルト）を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress  </span> </p> </td> 
   <td colname="col2"> <p>Lempel-Ziv-Welch(LZW)圧縮を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress  </span> </p> </td> 
   <td colname="col2"> <p>JPEGエンコーディングを使用します。 <span class="codeph"> <span class="varname"> sourceFile </span> </span>にアルファデータが含まれる場合は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality  &lt;&gt; quality  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>JPEG画質(0 ～ 100;初期設定は95です)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplecrominance  </span> </p> </td> 
   <td colname="col2"> <p>JPEGクロマダウンサンプリングを無効にします（カラーテキストとグラフィックの品質が向上します）。 これは、CMYKまたはグレースケールの出力画像には影響しません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm  &lt;&gt; amount  </span>&gt;  &lt;&gt; radius  </span>&gt; threshold  &lt;&gt; &gt;  </span> &lt;&gt;  </span>monochrome &gt;  </span><span class="varname"><span class="varname"><span class="varname"><span class="varname"> </span></span></span></span></p> </td> 
   <td colname="col2"> <p>アンシャープマスクをサブサンプルピラミッドレベルに適用します。 詳細は<a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a>を参照してください。 （最大解像度の画像には適用されません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath  </span> </p> </td> 
   <td colname="col2"> <p>ソースファイル内にクリップパスが存在する場合は、そのパスを使用して、関連するアルファデータを作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi  &lt;&gt; dpi  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p><span class="codeph"> <span class="varname"> destFile </span> </span>の印刷解像度(dpi);指定しなかった場合、<span class="codeph"> srcFile </span>の印刷解像度は<span class="codeph"> <span class="varname"> destFile </span> </span>にコピーされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocrop  &lt;&gt; corner  </span>&gt;  &lt;&gt; mode &gt; tolerance  </span>&gt; infoFile  &lt;&gt;  </span> &lt;&gt;  </span>&gt;  </span><span class="varname"><span class="varname"><span class="varname"><span class="varname"> </span></span></span></span></p> </td> 
   <td colname="col2"> <p>切り抜き長方形を計算して、べた塗りの背景を最小限にします。 自動切り抜きアルゴリズムによって画像全体が切り抜かれる場合、切り抜き情報は出力されません。 </p> <p>画像を変換せずに切り抜き長方形を計算するには、<span class="codeph"> -autocrop </span>を指定し、<span class="codeph"> -convert </span>を指定せず、<span class="codeph"> <span class="varname"> destFileを指定しません。</span> </span></p>

<p><i><b>corner</b></i> - ul | ur | ll | lr </p>
   <p> シードポイントを使用する画像の隅を指定します。 modeが1の場合は無視されます。</p>
   <p><i><b>mode</b></i> - 0 | 1</p>
   <p>0に設定すると、指定した隅のピクセルのカラーに基づいて切り抜かれます。アルファデータがソースイメージに関連付けられている場合、事前に乗算されたカラーデータに対して機能します。</p>
   <p>1に設定すると、アルファデータに基づいて切り抜きが行われます。cornerは無視され、0は常にシード値です。アルファデータがソース画像に関連付けられていない場合、切り抜きは適用されません。</p> 
   <p><i><b>tolerance</b></i>  — マッチ許容値。実数0.0 ～ 1.0。ピクセルコンポーネントの値との一致に関する許容値を指定します。 完全一致の場合は0に設定します。</p>
   <p><i><b>infoFile</b></i>  — 切り抜き情報データの書き込み先となるXML出力ファイルのパスと名前。</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData  </span> </p> </td> 
   <td colname="col2"> <p>XMPメタデータを（利用可能な場合） <span class="codeph"> <span class="varname"> </span> </span>から<span class="codeph"> <span class="varname"> destFile </span> </span>に変更なしでコピーします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile  </span> </p> </td> 
   <td colname="col2"> <p> ICCカラープロファイルを<span class="codeph"> <span class="varname"> destFile </span> </span>に埋め込みます(プロファイルはデフォルトで埋め込まれません)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile  &lt;&gt; file  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>ICCプロファイルファイルのパスと名前。 <span class="codeph"> <span class="varname"> sourceFile </span> </span>のカラースペースを定義し、そのピクセルタイプと一致させる必要があります。 プロファイルが<span class="codeph"> <span class="varname"> sourceFile </span> </span>に埋め込まれていない場合にのみ指定します。これは埋め込みプロファイルを上書きするためです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile  &lt;&gt; file  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>ICCプロファイルファイルのパスと名前。 <span class="codeph"> <span class="varname"> destFile </span> </span>のピクセルタイプとカラースペースを定義します。 <span class="codeph"> <span class="varname"> sourceFile </span> </span>に埋め込みプロファイルがある場合、または<span class="codeph"> -imageprofile </span>が指定されている場合、ICはこのプロファイルに変換します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptical  </span> </p> </td> 
   <td colname="col2"> <p>カラースペース変換に対する知覚的なレンダリングインテント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric  </span> </p> </td> 
   <td colname="col2"> <p> カラースペース変換の相対的な色域を保持レンダーインテント（初期設定） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimetric  </span> </p> </td> 
   <td colname="col2"> <p>カラースペース変換用の絶対的な色域を保持レンダリングインテント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation  </span> </p> </td> 
   <td colname="col2"> <p>カラースペース変換用の彩度レンダリングインテント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation  </span> </p> </td> 
   <td colname="col2"> <p>特定の色変換に対するブラックポイント補正の無効化 </p> <p>デフォルトで有効です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8  </span> </p> </td> 
   <td colname="col2"> <p>色変換時にディザリング（エラー拡散）を無効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintenancepixeltype  </span> </p> </td> 
   <td colname="col2"> <p> CMYKからRGBへの自動変換を無効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress  </span> </p> </td> 
   <td colname="col2"> <p>JPEG入力画像の強制デコードおよび再エンコード。 </p> <p> <b>注意：このオプションを</b> 適用すると、画質が低下する場合があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2  </span> </p> </td> 
   <td colname="col2"> <p>標準品質（バイリニア）の再サンプリングフィルタを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8  </span> </p> </td> 
   <td colname="col2"> <p>より高いクォリティ（ランチョスウィンドウ）の再サンプリングフィルタ（デフォルト）を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix  </span> </p> </td> 
   <td colname="col2"> <p>より高い画質(FlashPix)のリサンプリングフィルタを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp  </span> </p> </td> 
   <td colname="col2"> <p>Photoshopスタイルの8x8バイキュービックシャープフィルターを使用したダウンサンプル </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage  </span> </p> </td> 
   <td colname="col2"> <p> 最初のオプションとして指定した場合、無効なオプションが見つかった場合に、使用状況情報の出力を抑制します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -上書き </span> </p> </td> 
   <td colname="col2"> <p>既存の<span class="codeph"> <span class="varname"> destFile </span> </span>を上書きできます。 デフォルトでは、上書きを防ぐために、ファイル名に数値のサフィックスが追加されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> スキフィデン  </span> </p> </td> 
   <td colname="col2"> <p>非表示のソースファイルを無視します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror  </span> </p> </td> 
   <td colname="col2"> <p>エラーが発生した場合は処理を停止しないでください。 複数のファイルを処理する場合にのみ有効です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile  &lt;&gt; file  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>ログファイルのパスと名前（デフォルトは<span class="codeph"> stdout </span>）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel  &lt;&gt; level  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>ログレベル。 </p> 
   <p>&lt; 0=""&gt;</p>
   <p>0 — 処理するリストファイル。</p>
   <p>1 — 不要なファイルの追加レポート。</p>
   <p>2 — 進行状況のレポート追加。</p>
   <p>3 — 検出されたすべてのファイルの追加レポート。</p>
   <p>4 — ファイルレベルでの追加進行状況レポート。</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend  </span> </p> </td> 
   <td colname="col2"> <p>ログファイルに追加（デフォルト） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend  </span> </p> </td> 
   <td colname="col2"> <p>ログファイルを上書きします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogressmsec  &lt;&gt; msec  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>loglevel 2以降のログ間隔（ミリ秒）（デフォルトは3000）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem  &lt;&gt; bytes  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>メモリ使用量の制限。 10 MB以上にする必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent  &lt;&gt; percent  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>メモリ使用量の制限。 デフォルトは、物理メモリの25%です。 <span class="codeph"> maxmem </span>も<span class="codeph"> maxmempercent </span>も明示的に設定されていない場合は、maxmempercentのデフォルト値が使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -バージョン </span> </p> </td> 
   <td colname="col2"> <p> このユーティリティのバージョン情報を返します。 他のオプションは使用しないで指定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## サポートされる入力画像形式{#section-ab13d941d6724e65b9f84b62d949d31c}

次の表に、ICでサポートされる画像ファイル形式と形式リストを示します。

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> 形式</b> </p> </th> 
   <th class="entry"> <p> <b> Pixel </b> <b> TypeBits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> ビット/チャン</b> </p> </th> 
   <th class="entry"> <p> <b> 圧縮</b> </p> </th> 
   <th class="entry"> <p> <b> 説明</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> （Windowsビットマップ） </p> </td> 
   <td> <p> RGB |インデックス付き </p> </td> 
   <td> <p> 3 | 5/6 | 8 </p> </td> 
   <td> <p> 未圧縮 | RLE </p> </td> 
   <td> <p> 5/6ビット/チャネルは、16ビットRGB (5-5-5および5-6-5ビット/チャネル)のサポートを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (Encapsulated Postscript) </p> </td> 
   <td> <p> CMYK | RGB | gray </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII | ASCII85 |バイナリ | JPEG </p> </td> 
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
   <td> <p> 索引付き </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> LZW </p> </td> 
   <td> <p> 指定した場合、パレットの透明度の値はアルファに変換されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG</b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMYK | RGB | gray </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | gray | grayA </p> </td> 
   <td> <p> 3 | 8 | 16 </p> </td> 
   <td> <p> 未圧縮 |圧縮済み </p> </td> 
   <td> <p> 結合された画像のみ；レイヤーと余分なチャネルは無視されます。 </p> </td> 
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
   <td> <p> RGB | RGBA | gray | grayA |インデックス付き </p> </td> 
   <td> <p> 3 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> 圧縮 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | gray | grayA |インデックス付き </p> </td> 
   <td> <p> 3 | 8 | 16 </p> </td> 
   <td> <p> 未圧縮 | ZIP | LZW | JPEG | CCITT RLE | CCITT G3 | CCITT G4 |パックビット </p> </td> 
   <td> <p> 最初に関連付けられたアルファチャネルを除き、余分なチャネルは無視されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

埋め込まれたICCプロファイルは、EPS、JPG、PSD、PNGおよびTIFFファイルで認識されます。

埋め込まれたパスとXMPメタデータは、EPS、JPG、PSDおよびTIFFファイルで認識されます。

## 例 {#section-3c1986b30315431989bd76b1ee5bef6d}

1つの画像を最高画質で変換し、同じフォルダーに保つ：

`ic -convert src/myFile.png src/myFile.tif`

*`srcFolder`*&#x200B;内のすべての画像をJPEGエンコードピラミッドTIFFに変換し、*`destFolder`*&#x200B;に配置します。

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

*`srcFolder`*&#x200B;内のすべての画像を変換します。 JPGファイルのエンコードされた画像データは、これらの画像の残りの画像角錐の部分に対して、また、すべての非JPG入力ファイルの出力画像全体に対して、最大解像度、損失なしのLZW圧縮に使用されます。 ピクセルタイプ、埋め込みカラープロファイル、XMPメタデータなど。 の値は維持されます。

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
