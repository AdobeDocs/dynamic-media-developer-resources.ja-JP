---
description: 画像変換ユーティリティ。
solution: Experience Manager
title: ic
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ab653aae-532b-4f3d-8541-f6296fbf9172
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1204'
ht-degree: 1%

---

# ic {#ic}

画像変換ユーティリティ。

`ic` は、画像ファイルを最適化されたピラミッドTIFF形式 (PTIFF) に変換するコマンドラインツールです。 画像サービングでは変換処理をおこなわずに画像を処理できますが、512 x 512 ピクセルを超えるすべての画像を PTIFF に変換することをお勧めします。 この変換により、最適なサーバーパフォーマンスとリソース使用量を確保し、応答時間を最小限に抑えることができます。

写真コンテンツを含む PTIFF ファイルは、JPEGエンコード ( `-jpegcompress`) をクリックします。 コンピューターが生成したコンテンツは、ロスレス圧縮 ( `-deflatecompress` または `-lzwcompress`) をクリックします。 色変換や画素型変換が必要でない限り、品質の劣化を避けるため、JPEGソース画像データを復号せずに PTIFF に転送する。 この場合、指定した圧縮オプションは低解像度のピラミッドレベルにのみ適用されます。

大きな画像を変換しない場合は、使用するメモリ量を制御するパラメータを設定する必要はありません。 しかし、もしそうなら、 `ic` メモリを増やすには、 `-maxmem` 以下に説明する設定。 必要なメモリ量を計算する際の経験則として、画像の幅に画像の高さにチャネル数を掛けることが適しています。 例えば、アルファ倍の 3 のRGB画像の場合は 4 です。 さらに、チャネルが 8 の 2 倍ではなく 16 ビット/コンポーネントの場合、最終結果が得られます。

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
   <td colname="col2"> <p>単一出力 PTIFF ファイル（SourceDirectory と一緒に使用する場合は無効）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>入力画像を含むフォルダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>出力 PTIFF ファイルが書き込まれるフォルダー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-36a2dcfa39824d29b69547c432366219}

成功した場合は 0。 エラーが発生した場合、0 以外の値が返され、エラーの詳細が `stderr`.

## オプション {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -未圧縮 </span> </p> </td> 
   <td colname="col2"> <p>出力画像を圧縮しないでください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress </span> </p> </td> 
   <td colname="col2"> <p>deflate (zip) 圧縮（デフォルト）を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress </span> </p> </td> 
   <td colname="col2"> <p>Lempel-Ziv-Welch(LZW) 圧縮を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress </span> </p> </td> 
   <td colname="col2"> <p>JPEGエンコーディングを使用。 次の場合は無視 <span class="codeph"> <span class="varname"> sourceFile </span> </span> には、アルファデータが含まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality &lt; <span class="varname"> 品質 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>JPEG画質（0 ～ 100、デフォルトは 95）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplecrominance </span> </p> </td> 
   <td colname="col2"> <p>JPEGのクロマダウンサンプリングを無効にします（カラーテキストとグラフィックの品質を向上させます）。 これは、CMYK またはグレースケールの出力画像には影響しません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm &lt; <span class="varname"> 量 </span>&gt; &lt; <span class="varname"> 半径 </span>&gt; &lt; <span class="varname"> しきい値 </span>&gt; &lt; <span class="varname"> モノクロ </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>アンシャープマスクをサブサンプルピラミッドレベルに適用します。 詳しくは、 <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a> 」を参照してください。 （最大解像度の画像には適用されません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath </span> </p> </td> 
   <td colname="col2"> <p>ソースファイル内のクリップパス（存在する場合）を使用して、関連するアルファデータを作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi &lt; <span class="varname"> dpi </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>用の印刷解像度 (dpi) <span class="codeph"> <span class="varname"> destFile </span> </span>を指定しない場合、の印刷解像度 <span class="codeph"> srcFile </span> が次の場所にコピーされます： <span class="codeph"> <span class="varname"> destFile </span> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocrop &lt; <span class="varname"> corner </span>&gt; &lt; <span class="varname"> mode </span>&gt; &lt; <span class="varname"> 許容値 </span>&gt; &lt; <span class="varname"> infoFile </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>切り抜き長方形を計算して、べた塗りの背景を最小限に抑えます。 自動切り抜きアルゴリズムによって画像全体が切り抜かれる場合、切り抜き情報は出力されません。 </p> <p>画像を変換せずに切り抜き長方形を計算するには、次のように指定します。 <span class="codeph"> -autocrop </span> なし <span class="codeph"> -convert </span> そして <span class="codeph"> <span class="varname"> destFile.</span> </span></p>

<p><i><b>corner</b></i> - ul | ur | ll | lr </p>
   <p> シードポイントを使用する画像のコーナーを指定します。 mode が 1 の場合は無視されます。</p>
   <p><i><b>mode</b></i> - 0 | 1</p>
   <p>指定したコーナーピクセルのカラーに基づいて切り抜くには 0 に設定します。アルファデータがソースイメージに関連付けられている場合は、プリマルチプライカラーデータに対して機能します。</p>
   <p>アルファデータに基づいて切り抜くには 1 に設定します。角は無視され、常にシード値は 0 になります。アルファデータがソース画像に関連付けられていない場合は、切り抜きは適用されません。</p> 
   <p><i><b>許容値</b></i>  — 一致許容値。 0.0 ～ 1.0 の実数値。ピクセルコンポーネントの値の一致に対する許容値を指定します。 完全に一致する場合は 0 に設定します。</p>
   <p><i><b>infoFile</b></i>  — 切り抜き情報データが書き込まれる XML 出力ファイルのパスと名前。</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData </span> </p> </td> 
   <td colname="col2"> <p>XMPメタデータ（使用可能な場合）を次の場所からコピー <span class="codeph"> <span class="varname"> sourceFile </span> </span> から <span class="codeph"> <span class="varname"> destFile </span> </span> 変更なしで </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile </span> </p> </td> 
   <td colname="col2"> <p> に ICC カラープロファイルを埋め込む <span class="codeph"> <span class="varname"> destFile </span> </span>（使用可能な場合）（デフォルトではプロファイルが埋め込まれません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt; <span class="varname"> ファイル </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ICC プロファイルファイルのパスと名前。 のカラースペースを定義します。 <span class="codeph"> <span class="varname"> sourceFile </span> </span> とは、そのピクセルタイプに一致する必要があります。 プロファイルが <span class="codeph"> <span class="varname"> sourceFile </span> </span>埋め込みプロファイルを上書きするので、を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt; <span class="varname"> ファイル </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ICC プロファイルファイルのパスと名前。 のピクセルタイプとカラースペースを定義します。 <span class="codeph"> <span class="varname"> destFile </span> </span>. 次の場合、IC はこのプロファイルに変換されます。 <span class="codeph"> <span class="varname"> sourceFile </span> </span> には、埋め込まれたプロファイルがあるか、 <span class="codeph"> -imageprofile </span> も指定されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptual </span> </p> </td> 
   <td colname="col2"> <p>カラースペース変換の知覚的レンダリングインテント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric </span> </p> </td> 
   <td colname="col2"> <p> 「相対的な色域を維持」は、カラースペース変換のレンダリング方法（デフォルト）です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColormetric </span> </p> </td> 
   <td colname="col2"> <p>「絶対的な色域を維持」は、カラースペース変換のレンダリング方法です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation </span> </p> </td> 
   <td colname="col2"> <p>カラースペース変換の彩度レンダリングの方法。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation </span> </p> </td> 
   <td colname="col2"> <p>特定の色変換の黒点補正を無効にする </p> <p>デフォルトで有効です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8 </span> </p> </td> 
   <td colname="col2"> <p>色変換時にディザリング（エラー拡散）を無効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintenancepixetype </span> </p> </td> 
   <td colname="col2"> <p> CMYK から CMYK への自動変換を無効にします。RGB </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress </span> </p> </td> 
   <td colname="col2"> <p>デコードと再エンコードを強制的にJPEG入力画像にします。 </p> <p> <b>注意：</b> このオプションを適用すると、画質が低下する場合があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2 </span> </p> </td> 
   <td colname="col2"> <p>標準品質（バイリニア）の再サンプリングフィルタを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8 </span> </p> </td> 
   <td colname="col2"> <p>より高品質（Lanczos ウィンドウ）の再サンプリングフィルタを使用します（デフォルト）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix </span> </p> </td> 
   <td colname="col2"> <p>より高品質の (FlashPix) 再サンプリングフィルタを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp </span> </p> </td> 
   <td colname="col2"> <p>Photoshopスタイル 8x8 バイキュービックシャープフィルターを使用したダウンサンプル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">  — 能下 </span> </p> </td> 
   <td colname="col2"> <p> 1 番目のオプションとして指定した場合、無効なオプションが見つかった場合に使用情報の出力を抑制します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -上書き </span> </p> </td> 
   <td colname="col2"> <p>既存の <span class="codeph"> <span class="varname"> destFile </span> </span>. デフォルトでは、上書きを防ぐために、数値のサフィックスがファイル名に追加されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphidden </span> </p> </td> 
   <td colname="col2"> <p>非表示のソースファイルを無視します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror </span> </p> </td> 
   <td colname="col2"> <p>エラーが発生した場合に処理を停止しないでください。 複数のファイルを処理する場合にのみ効果があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile &lt; <span class="varname"> ファイル </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ログファイルのパスと名前 ( デフォルトは <span class="codeph"> stdout </span>) をクリックします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel &lt; <span class="varname"> レベル </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ログレベル。 </p> 
   <p>&lt; 0 — ログが無効です。</p>
   <p>0 — 処理するファイルのリスト。</p>
   <p>1 — 不要なファイルに対するレポートを追加します。</p>
   <p>2 — 進行状況レポートを追加します。</p>
   <p>3 — 発生したすべてのファイルに関するレポートを追加します。</p>
   <p>4 — 進行状況レポートをファイルレベルで追加します。</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend </span> </p> </td> 
   <td colname="col2"> <p>ログファイルに追加します（デフォルト）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend </span> </p> </td> 
   <td colname="col2"> <p>ログファイルを上書きします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogresssmsec &lt; <span class="varname"> ミリ秒 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>loglevel 2 以降のログ間隔（ミリ秒）（デフォルトは 3000）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem &lt; <span class="varname"> バイト </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>メモリ使用量の制限。 10 MB 以上にする必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent &lt; <span class="varname"> 割合 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>メモリ使用量の制限。 デフォルトは、物理メモリの 25 %です。 どちらでもない場合 <span class="codeph"> maxmem </span> nor <span class="codeph"> maxmempercent </span> は、maxmempercent デフォルトを使用して明示的に設定されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -バージョン </span> </p> </td> 
   <td colname="col2"> <p> このユーティリティのバージョン情報を返します。 他のオプションは指定しないでください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## サポートされる入力画像形式 {#section-ab13d941d6724e65b9f84b62d949d31c}

次の表に、IC でサポートされる画像ファイル形式と形式のオプションを示します。

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> 形式</b> </p> </th> 
   <th class="entry"> <p> <b> ピクセルタイプ</b> <b> ビット/チャン</b> </p> </th> 
   <th class="entry"> <p> <b> ビット/チャン</b> </p> </th> 
   <th class="entry"> <p> <b> 圧縮</b> </p> </th> 
   <th class="entry"> <p> <b> 説明</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> （Windows ビットマップ） </p> </td> 
   <td> <p> RGB |インデックス付き </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> 非圧縮 | RLE </p> </td> 
   <td> <p> 5/6 ビット/チャネルは、16 ビットRGB(5-5-5および5-6-5ビット/チャネル ) のサポートを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (Encapsulated Postscript) </p> </td> 
   <td> <p> CMYK |RGB | gray </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII | ASCII85 |バイナリ |JPEG </p> </td> 
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
   <td> <p> インデックス付き </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> LZW </p> </td> 
   <td> <p> 存在する場合、パレットの透明度の値はアルファに変換されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG</b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMYK |RGB | gray </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK | CMYKA |RGB | RGBA | gray | grayA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 非圧縮 |圧縮 </p> </td> 
   <td> <p> 結合された画像のみ。レイヤーと追加のチャンネルは無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RLE </p> </td> 
   <td> <p> ビットマップデータのみ。ベクトルデータは無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB | RGBA | gray | grayA |インデックス付き </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> 圧縮 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK | CMYKA |RGB | RGBA | gray | grayA |インデックス付き </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 非圧縮 | ZIP | LZW |JPEG | CCITT RLE | CCITT G3 | CCITT G4 | Packbits </p> </td> 
   <td> <p> 最初に関連付けられたアルファチャンネルを除き、追加のチャンネルは無視されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

埋め込み ICC プロファイルは、EPS、JPG、PSD、PNG、TIFFファイルで認識されます。

埋め込みパスとXMPメタデータは、EPS、JPG、PSD、TIFFファイルで認識されます。

## 例 {#section-3c1986b30315431989bd76b1ee5bef6d}

1 つの画像を最高品質で変換し、同じフォルダーに保持します。

`ic -convert src/myFile.png src/myFile.tif`

でのすべての画像の変換 *`srcFolder`* をJPEGエンコードしたピラミッドTIFFに追加し、 *`destFolder`*:

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

でのすべての画像の変換 *`srcFolder`*. JPGファイルの符号化画像データは、これらの画像の残りの画像ピラミッドの全解像度レベル、ロスレス LZW 圧縮、およびすべての非JPG入力ファイルの全出力画像に使用される。 ピクセルタイプ、埋め込まれたカラープロファイル、XMPメタデータなど。 は維持されます。

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
