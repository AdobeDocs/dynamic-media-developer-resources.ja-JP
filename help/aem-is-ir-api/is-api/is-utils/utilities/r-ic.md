---
description: 画像変換ユーティリティ
solution: Experience Manager
title: ic
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: ab653aae-532b-4f3d-8541-f6296fbf9172
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1209'
ht-degree: 2%

---

# ic {#ic}

画像変換ユーティリティ

`ic` は、画像ファイルを最適化されたピラミッドTIFF形式(PTIFF)に変換するコマンドラインツールです。画像サービングは変換なしで画像を処理できますが、512 x 512ピクセルを超えるすべての画像をPTIFFに変換することをお勧めします。 この変換により、サーバーのパフォーマンスとリソースの使用量が最適化され、応答時間が最小限に抑えられます。

写真コンテンツを含むPTIFFファイルは、JPEGエンコードすることをお勧めします（`-jpegcompress`を指定）。 コンピューターで生成されたコンテンツは、可逆圧縮（`-deflatecompress`または`-lzwcompress`）のメリットが得られます。 色変換や画素型変換が必要でない限り、画質劣化を避けるため、JPEGソース画像データをデコードせずにPTIFFに転送する。 この場合、指定した圧縮オプションは、低解像度のピラミッドレベルにのみ適用されます。

大きな画像を変換しない場合は、使用するメモリ量を制御するパラメータを設定する必要はありません。 ただし、メモリがある場合は、以下に示す`-maxmem`設定を使用して、`ic`メモリを増やします。 必要なメモリ量を計算する際の経験則として、画像の幅に画像の高さにチャネル数を掛けるのが良いです。 例えば、アルファ倍が3のRGB画像の場合は4です。 さらに、チャネルが8ではなく16ビット/コンポーネントの場合、最終結果は2倍になります。

## 使用方法 {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]`*`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]`*`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]`*`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>options</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>コマンドオプション（以下を参照）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> <i>sourceFile</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>単一入力画像ファイル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span> </span> </p> </td> 
   <td colname="col2"> <p>単一出力PTIFFファイル（SourceDirectoryと一緒に使用する場合は無効）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>入力画像を含むフォルダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>出力PTIFFファイルの書き込み先のフォルダー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-36a2dcfa39824d29b69547c432366219}

成功した場合は0。 エラーが発生した場合は、ゼロ以外の値が返され、エラーの詳細が`stderr`に送信されます。

## オプション {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -未圧縮 </span> </p> </td> 
   <td colname="col2"> <p>出力画像を圧縮しないでください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress  </span> </p> </td> 
   <td colname="col2"> <p>deflate(zip)圧縮を使用します（デフォルト）。 </p> </td> 
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
   <td colname="col2"> <p>JPEG画質(0～100、初期設定は95)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplechrominance  </span> </p> </td> 
   <td colname="col2"> <p>JPEGクロマダウンサンプリングを無効にする（カラーテキストとグラフィックの品質を向上させることができます）。 これは、CMYKまたはグレースケールの出力画像には影響しません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm  &lt;&gt; amount  </span>&gt;  &lt;&gt; radius  </span>&gt;  &lt;&gt; threshold  </span>&gt;  &lt;&gt; monochrome  </span>&gt;  </span><span class="varname"><span class="varname"><span class="varname"><span class="varname"> </span></span></span></span></p> </td> 
   <td colname="col2"> <p>サブサンプリングされたピラミッドレベルにアンシャープマスクを適用します。 詳しくは、 <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a>を参照してください。 （最大解像度の画像には適用されません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath  </span> </p> </td> 
   <td colname="col2"> <p>ソースファイル内にクリップパスがある場合は、そのパスを使用して、関連するアルファデータを作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi  &lt;&gt; dpi  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p><span class="codeph"> <span class="varname"> destFile </span> </span>の印刷解像度(dpi)。指定しなかった場合、 <span class="codeph"> srcFile </span>の印刷解像度が<span class="codeph"> <span class="varname"> destFile </span> </span>にコピーされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocrop  &lt;&gt; corner  </span>&gt;  &lt;&gt; mode  </span>&gt;  &lt;&gt; tolerance  </span>&gt;  &lt;&gt; infoFile  </span>&gt;  </span><span class="varname"><span class="varname"><span class="varname"><span class="varname"> </span></span></span></span></p> </td> 
   <td colname="col2"> <p>塗りつぶし長方形を計算して、べた塗りの背景を最小限に抑えます。 自動切り抜きアルゴリズムによって画像全体が切り抜かれる場合、切り抜き情報は出力されません。 </p> <p>画像を変換せずに切り抜き長方形を計算するには、 <span class="codeph"> -autocrop </span>を<span class="codeph">なしで —convert </span>を指定し、 <span class="codeph"> <span class="varname"> destFileを指定しません。 </span> </span></p>

<p><i><b>corner</b></i>  - ul | ur | ll | lr </p>
   <p> シードポイントを使用する画像のコーナーを指定します。 modeが1の場合は無視されます。</p>
   <p><i><b>mode</b></i>  - 0 | 1</p>
   <p>0に設定すると、指定した角のピクセルのカラーに基づいて切り抜かれます。アルファデータがソースイメージに関連付けられている場合、プリマルチプライカラーデータに対して機能します。</p>
   <p>アルファデータに基づいて切り抜くには、1に設定します。cornerは無視され、 0は常にシード値です。アルファデータがソース画像に関連付けられていない場合、切り抜きは適用されません。</p> 
   <p><i><b>tolerance</b></i>  — 一致許容値。実数値0.0 ～ 1.0。ピクセルコンポーネントの値の一致に対する許容値を指定します。 完全一致の場合は0に設定します。</p>
   <p><i><b>infoFile</b></i>  — 切り抜き情報データの書き込み先となるXML出力ファイルのパスと名前。</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData  </span> </p> </td> 
   <td colname="col2"> <p>XMPメタデータを（使用可能な場合） <span class="codeph"> <span class="varname"> sourceFile </span> </span>から<span class="codeph"> <span class="varname"> destFile </span> </span>に変更せずにコピーします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile  </span> </p> </td> 
   <td colname="col2"> <p> ICCカラープロファイルを<span class="codeph"> <span class="varname"> destFile </span> </span>に埋め込みます（使用可能な場合）（デフォルトではプロファイルは埋め込まれません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile  &lt;&gt; file  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>ICCプロファイルファイルのパスと名前。 <span class="codeph"> <span class="varname"> sourceFile </span> </span>のカラースペースを定義し、そのピクセルタイプと一致する必要があります。 <span class="codeph"> <span class="varname"> sourceFile </span> </span>にプロファイルが埋め込まれていない場合にのみ指定します。これは、埋め込みプロファイルが上書きされるためです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofileファ &lt;&gt; イル </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>ICCプロファイルファイルのパスと名前。 <span class="codeph"> <span class="varname"> destFile </span> </span>のピクセルタイプとカラースペースを定義します。 <span class="codeph"> <span class="varname"> sourceFile </span> </span>に埋め込みプロファイルがある場合、または<span class="codeph"> -imageprofile </span>も指定されている場合、ICはこのプロファイルに変換されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptical  </span> </p> </td> 
   <td colname="col2"> <p>知覚的に、カラースペース変換の意図をレンダリングする。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric  </span> </p> </td> 
   <td colname="col2"> <p> 「相対的な色域を維持」は、カラースペース変換のレンダリングインテントです（デフォルト）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimetric  </span> </p> </td> 
   <td colname="col2"> <p>「絶対的な色域を維持」は、カラースペース変換のレンダリングインテントです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation  </span> </p> </td> 
   <td colname="col2"> <p>彩度レンダリングカラースペース変換の目的。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation  </span> </p> </td> 
   <td colname="col2"> <p>特定の色変換のブラックポイント補正の無効化 </p> <p>デフォルトで有効です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8  </span> </p> </td> 
   <td colname="col2"> <p>色変換時にディザリング（エラー拡散）を無効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintenancepixetype  </span> </p> </td> 
   <td colname="col2"> <p> CMYKからRGBへの自動変換を無効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress  </span> </p> </td> 
   <td colname="col2"> <p>JPEG入力画像のデコードと再エンコードを強制的に実行します。 </p> <p> <b>注意：</b> このオプションを適用すると、画質が低下する場合があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2  </span> </p> </td> 
   <td colname="col2"> <p>標準品質（バイリニア）の再サンプリングフィルターを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8  </span> </p> </td> 
   <td colname="col2"> <p>より高品質（Lanczosウィンドウ）の再サンプリングフィルタ（デフォルト）を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix  </span> </p> </td> 
   <td colname="col2"> <p>より高品質の(FlashPix)再サンプリングフィルタを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp  </span> </p> </td> 
   <td colname="col2"> <p>Photoshopスタイル8x8バイキュービックシャープフィルターを使用したダウンサンプル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage  </span> </p> </td> 
   <td colname="col2"> <p> 1番目のオプションに指定した場合、無効なオプションが見つかった場合に使用情報の出力を抑制します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -上書き </span> </p> </td> 
   <td colname="col2"> <p>既存の<span class="codeph"> <span class="varname"> destFile </span> </span>を上書きできます。 デフォルトでは、上書きを防ぐために、ファイル名に数値サフィックスが追加されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphidden  </span> </p> </td> 
   <td colname="col2"> <p>非表示のソースファイルを無視します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror  </span> </p> </td> 
   <td colname="col2"> <p>エラーが発生した場合に処理を停止しないでください。 複数のファイルを処理する場合にのみ効果があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile  &lt;&gt; file  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>ログファイルのパスと名前（デフォルトは<span class="codeph"> stdout </span>）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel  &lt;&gt; level  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>ログレベル。 </p> 
   <p>&lt; 0=""&gt;</p>
   <p>0 — 処理するファイルのリスト。</p>
   <p>1 — 不要なファイルに関するレポートを追加します。</p>
   <p>2 — 進行状況レポートを追加します。</p>
   <p>3 — すべてのファイルに関するレポートを追加します。</p>
   <p>4 — 進行状況レポートをファイルレベルで追加します。</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend  </span> </p> </td> 
   <td colname="col2"> <p>ログファイルに追加（デフォルト）。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> -maxmemバ &lt;&gt; イト </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>メモリ使用制限。 10 MB以上にする必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent  &lt;&gt; percent  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>メモリ使用制限。 デフォルトは物理メモリの25%です。 <span class="codeph"> maxmem </span>も<span class="codeph"> maxmempercent </span>も明示的に設定されていない場合は、maxmempercentのデフォルトが使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -バージョン </span> </p> </td> 
   <td colname="col2"> <p> このユーティリティのバージョン情報を返します。 他のオプションは指定しないでください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## サポートされる入力画像形式 {#section-ab13d941d6724e65b9f84b62d949d31c}

次の表に、ICでサポートされる画像ファイル形式と形式のオプションを示します。

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
   <td> <p> 非圧縮 | RLE </p> </td> 
   <td> <p> 5/6ビット/チャネルは、16ビットRGB(5-5-5および5-6-5ビット/チャネル)のサポートを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> （カプセル化されたPostscript） </p> </td> 
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
   <td> <p> インデックス </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> LZW </p> </td> 
   <td> <p> 存在する場合、パレットの透明度の値はアルファに変換されます。 </p> </td> 
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
   <td> <p> 非圧縮 |圧縮 </p> </td> 
   <td> <p> 結合された画像のみレイヤーと追加のチャンネルは無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RLE </p> </td> 
   <td> <p> ビットマップデータのみベクトルデータは無視されます。 </p> </td> 
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
   <td> <p> 非圧縮 | ZIP | LZW | JPEG | CCITT RLE | CCITT G3 | CCITT G4 | Packbits </p> </td> 
   <td> <p> 最初に関連付けられたアルファチャンネルを除き、追加のチャンネルは無視されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

埋め込みICCプロファイルは、EPS、JPG、PSD、PNG、TIFFファイルで認識されます。

埋め込みパスとXMPメタデータは、EPS、JPG、PSDおよびTIFFファイルで認識されます。

## 例 {#section-3c1986b30315431989bd76b1ee5bef6d}

1つの画像を最高画質で変換し、同じフォルダーに保持します。

`ic -convert src/myFile.png src/myFile.tif`

*`srcFolder`*&#x200B;内のすべての画像をJPEGエンコードされたピラミッドTIFFに変換し、 *`destFolder`*&#x200B;に配置します。

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

*`srcFolder`*&#x200B;内のすべての画像を変換します。 JPGファイルの符号化画像データは、これらの画像の残りの画像ピラミッドに対して、また、すべての非JPG入力ファイルの出力画像全体に対して、フル解像度、損失なしLZW圧縮に使用される。 ピクセルタイプ、埋め込みカラープロファイル、XMPメタデータなど。 が維持されます。

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
