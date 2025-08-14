---
description: 画像変換ユーティリティ。
solution: Experience Manager
title: ic
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ab653aae-532b-4f3d-8541-f6296fbf9172
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1239'
ht-degree: 0%

---

# ic {#ic}

画像変換ユーティリティ。

`ic` は、画像ファイルを最適化された Pyramid TIFF形式（PTIFF）に変換するコマンドラインツールです。 画像サービングでは変換せずに画像を処理できますが、512 x 512 ピクセルを超えるすべての画像を PTIFF に変換することをお勧めします。 この変換により、最適なサーバーパフォーマンスとリソース使用が確保され、応答時間が最小限に抑えられます。

写真コンテンツを含む PTIFF ファイルはJPEGでエンコードすることをお勧めします（`-jpegcompress` を指定します）。 コンピューター生成コンテンツには、可逆圧縮（`-deflatecompress` または `-lzwcompress`）の利点があります。 色変換や画素種変換が必要でない場合は、JPEGソース画像データをデコードせずに PTIFF に転送し、画質劣化を防止する。 この場合、指定した圧縮オプションは、低解像度のピラミッドレベルにのみ適用されます。

大きな画像を変換しない場合は、使用するメモリ量を制御するパラメーターを設定する必要はありません。 ただし、その場合は、以下に説明 `ic` る `-maxmem` 設定を使用して、より多くのメモリを提供します。 必要なメモリ量を計算する際の経験則として、画像の幅に画像の高さを掛け、さらにチャネル数を掛けます。 例えば、アルファ値が 3 倍のRGB画像には 4 を指定します。 さらに、チャネルがコンポーネントあたり 8 ビットではなく 16 ビットの場合、最終的な結果は 8 倍になります。

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
   <td colname="col2"> <p>単一の入力画像ファイル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span> </span> </p> </td> 
   <td colname="col2"> <p>単一出力 PTIFF ファイル （SourceDirectory で使用する場合は無効） </p> </td> 
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

成功した場合は 0 を返します。 エラーが発生した場合は 0 以外の値が返され、エラーの詳細が `stderr` に送信されます。

## オプション {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> – 非圧縮 </span> </p> </td> 
   <td colname="col2"> <p>出力画像を圧縮しないでください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress </span> </p> </td> 
   <td colname="col2"> <p>deflate （zip）圧縮を使用（デフォルト） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress </span> </p> </td> 
   <td colname="col2"> <p>Lempel-Ziv-Welch （LZW）圧縮を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress </span> </p> </td> 
   <td colname="col2"> <p>JPEG エンコーディングを使用します。 <span class="codeph"> <span class="varname"> sourceFile </span> </span> にアルファ版のデータが含まれる場合は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality &lt; <span class="varname"> quality </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>JPEGの画質（0 ～ 100、デフォルトは 95）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplechrominance </span> </p> </td> 
   <td colname="col2"> <p>JPEGのクロマダウンサンプリングを無効にします（テキストやグラフィックのカラーの品質を向上させることができます）。 これは、CMYK またはグレースケールの出力画像には影響しません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm &lt; <span class="varname"> amount </span>&gt; &lt; <span class="varname"> radius </span>&gt; &lt; <span class="varname"> threshold </span>&gt; &lt; <span class="varname"> monochrome </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>アンシャープマスクをサブサンプルのピラミッドレベルに適用します。 詳細は、<a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a> を参照してください。 （フル解像度の画像には適用されません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath </span> </p> </td> 
   <td colname="col2"> <p>関連付けられたアルファデータを作成するには、ソースファイルのクリップパスを使用します（存在する場合）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi &lt; <span class="varname"> dpi </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> <span class="varname"> destFile </span> </span> の印刷解像度（dpi）です。指定しない場合、srcFile <span class="codeph"> の印刷解像度 </span><span class="codeph"> destFile <span class="varname"> </span></span> コピーされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocrop &lt; <span class="varname"> corner </span>&gt; &lt; <span class="varname"> mode </span>&gt; &lt; <span class="varname"> tolerance </span>&gt; &lt; <span class="varname"> infoFile </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>単色の背景を最小限に抑えるために切り抜き長方形を計算します。 自動切り抜きアルゴリズムによって画像全体が切り抜かれる可能性がある場合、切り抜き情報は出力されません。 </p> <p><span class="codeph"> 画像を変換せずに切り抜き長方形を計算するには、-autocrop </span> without <span class="codeph"> -convert </span> and without <span class="codeph"> <span class="varname"> destFile.</span> </span> を指定します。</p>

<p><i><b>corner</b></i> - ul | ur | ll | lr </p>
   <p> シード ポイントを使用するイメージのコーナーを指定します。 mode が 1 の場合は無視されます。</p>
   <p><i><b>mode</b></i> - 0 | 1</p>
   <p>0 に設定すると、指定したコーナーピクセルのカラーに基づいて切り抜かれます。アルファデータがソースイメージに関連付けられている場合は、乗算済みのカラーデータに対して機能します。</p>
   <p>アルファデータに基づいて切り抜くには 1 に設定します。隅は無視され、0 は常にシード値です。アルファデータがソースイメージに関連付けられていない場合、切り抜きは適用されません。</p> 
   <p><i><b>tolerance</b></i> – 公差を一致させます。 実際の値は 0.0 ～ 1.0 です。ピクセル コンポーネント値に一致する許容値を指定します。 完全一致の場合は 0 に設定します。</p>
   <p><i><b>infoFile</b></i> – 切り抜き情報データが書き込まれる XML 出力ファイルのパスと名前。</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData </span> </p> </td> 
   <td colname="col2"> <p>可能な場合は、XMPのメタデータ <span class="codeph">、<span class="varname"> sourceFile </span> </span> から destFile <span class="codeph"> <span class="varname"></span> 変更 </span> ずにコピーします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile </span> </p> </td> 
   <td colname="col2"> <p> 使用可能な場合は、ICC カラープロファイル <span class="codeph"><span class="varname"> destFile </span> </span> に埋め込みます（デフォルトでは、プロファイルは埋め込まれていません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ICC プロファイルファイルのパスと名前。 sourceFile <span class="codeph"> <span class="varname"> のカラースペース </span> 定義 </span>、ピクセルタイプと一致する必要があります。 <span class="codeph"> sourceFile <span class="varname"> </span> にプロファイルが埋め込まれていない場合にのみ指定 </span> てください。これは、埋め込まれたプロファイルを上書きするからです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ICC プロファイルファイルのパスと名前。 <span class="codeph"> destFile <span class="varname"> </span> のピクセルタイプとカラースペース </span> 定義します。 <span class="codeph"> sourceFile <span class="varname"> </span> に埋め込まれたプロファイルがある場合 </span>、または – imageprofile <span class="codeph"> も指定されてい </span> 場合、IC はこのプロファイルに変換します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptual </span> </p> </td> 
   <td colname="col2"> <p>カラースペース変換の知覚的レンダリングインテント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric </span> </p> </td> 
   <td colname="col2"> <p> カラースペースコンバージョンの相対的な色域を維持レンダリングインテント（デフォルト）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimetric </span> </p> </td> 
   <td colname="col2"> <p>カラースペースコンバージョンの絶対的な色域を維持するレンダリングインテント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation </span> </p> </td> 
   <td colname="col2"> <p>カラースペース変換の彩度レンダリングインテント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation </span> </p> </td> 
   <td colname="col2"> <p>特定のカラーコンバージョンに対するブラックポイント補正の無効化 </p> <p>デフォルトで有効になっています。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8 </span> </p> </td> 
   <td colname="col2"> <p>カラー変換時のディザリング（エラーディフュージョン）を無効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintainpixeltype </span> </p> </td> 
   <td colname="col2"> <p> CMYK からRGBへの自動変換を無効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress </span> </p> </td> 
   <td colname="col2"> <p>JPEG入力画像のデコードと再エンコーディングを強制します。 </p> <p> <b> 注意：</b> このオプションを適用すると、画質が低下する場合があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2 </span> </p> </td> 
   <td colname="col2"> <p>標準品質（バイリニア）リサンプリングフィルターを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8 </span> </p> </td> 
   <td colname="col2"> <p>高品質（ランチョスウィンドウ）の再サンプリングフィルターを使用します（デフォルト）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix </span> </p> </td> 
   <td colname="col2"> <p>より高品質の（FlashPix）リサンプリングフィルタを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp </span> </p> </td> 
   <td colname="col2"> <p>Photoshop スタイルの 8x8 バイキュービックシャープフィルターを使用したダウンサンプル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage </span> </p> </td> 
   <td colname="col2"> <p> 最初のオプションで指定した場合、無効なオプションが見つかった場合に使用情報の出力を抑制します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> – 上書き </span> </p> </td> 
   <td colname="col2"> <p>destFile <span class="codeph"> <span class="varname"> の既存の </span> を上書き </span> きるようにします。 デフォルトでは、上書きを防ぐために、数値のサフィックスがファイル名に追加されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -</span> </p> </td> 
   <td colname="col2"> <p>隠しソースファイルを無視します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror </span> </p> </td> 
   <td colname="col2"> <p>エラーが発生した場合に処理を停止しない。 複数のファイルを処理する場合にのみ効果があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ログファイルのパスと名前（デフォルトは <span class="codeph"> stdout </span>）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel &lt; <span class="varname"> レベル </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ログレベル。 </p> 
   <p>&lt; 0 - ログが無効です。</p>
   <p>0 – 処理するファイルをリストします。</p>
   <p>1 – 不要なファイルのレポートを追加します。</p>
   <p>2 – 進捗レポートの追加</p>
   <p>3 – 発生したすべてのファイルに関するレポートを追加します。</p>
   <p>4 - ファイルレベルで進捗レポートを追加します。</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend </span> </p> </td> 
   <td colname="col2"> <p>ログファイルにを追加（デフォルト）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend </span> </p> </td> 
   <td colname="col2"> <p>ログファイルを上書き。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogressmssec &lt; <span class="varname"> msec </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ログレベル 2 以上のログ間隔（ミリ秒単位、デフォルトは 3000）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem &lt; <span class="varname"> バイト </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>メモリ使用制限。 10 MB 以上にする必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent &lt; <span class="varname"> percent </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>メモリ使用制限。 デフォルトは物理メモリの 25% です。 maxmem <span class="codeph"> も maxmempercent </span> も明示的 <span class="codeph"> 設定され </span> いない場合は、maxmempercent のデフォルトが使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -version </span> </p> </td> 
   <td colname="col2"> <p> このユーティリティのバージョン情報を返します。 を他のオプションなしで指定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## サポートされる入力画像形式 {#section-ab13d941d6724e65b9f84b62d949d31c}

以下の表に、IC でサポートされる画像ファイル形式と形式オプションを示します。

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> 形式 </b> </p> </th> 
   <th class="entry"> <p> <b> Pixel Type</b> <b> Bits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> ビット/ちゃん </b> </p> </th> 
   <th class="entry"> <p> <b> 圧縮 </b> </p> </th> 
   <th class="entry"> <p> <b> Notes</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> （Windows ビットマップ） </p> </td> 
   <td> <p> RGB | インデックス作成 </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> 非圧縮 | URL </p> </td> 
   <td> <p> 5/6 bit/channel は、16 ビット RGB （5-5-5 および 5-6-5 ビット/channel）のサポートを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td> EPS<b> す </b>。 <p> （Encapsulated Postscript） </p> </td> 
   <td> <p> CMYK |RGB |灰色 </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII | ASCII85 | バイナリ |JPEG </p> </td> 
   <td> <p> Photoshopで生成されたEPS ファイルのみがサポートされます。 </p> </td> 
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
   <td> <p> パレット内に透明度の値が存在する場合は、アルファに変換されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> JPG<b> す </b>。 <p> （JFIF/JPEG） </p> </td> 
   <td> <p> CMYK |RGB |灰色 </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK | CMYKA |RGB | RGBA |灰色 | grayA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 非圧縮 |圧縮 </p> </td> 
   <td> <p> 結合された画像のみ。レイヤーと追加のチャンネルは無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> 役割 </p> </td> 
   <td> <p> ビットマップデータのみ。ベクトルデータは無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB | RGBA |灰色 | grayA | インデックス作成 </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> 圧縮 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> TIFF<b> す </b>。 </td> 
   <td> <p> CMYK | CMYKA |RGB | RGBA |灰色 | grayA | インデックス作成 </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 非圧縮 |郵便番号 | LZW |JPEG | CCITT ルール | CCITT G3 | CCITT G4 | パッケージビット </p> </td> 
   <td> <p> 最初に関連付けられたアルファチャンネルを除き、追加のチャンネルは無視されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

埋め込まれた ICC プロファイルは、EPS、JPG、PSD、PNG およびTIFF ファイルで認識されます。

埋め込みパスとXMP メタデータは、EPS、JPG、PSDおよびTIFFの各ファイルで認識されます。

## 例 {#section-3c1986b30315431989bd76b1ee5bef6d}

単一の画像を最高品質で変換し、同じフォルダーに保持する：

`ic -convert src/myFile.png src/myFile.tif`

*`srcFolder`* 内のすべての画像をJPEGでエンコードされた Pyramid TIFF に変換し、*`destFolder`* に配置します。

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

*`srcFolder`* 内のすべての画像を変換します。 JPG ファイルのエンコードされた画像データは、これらの画像の残りの画像ピラミッドと、すべての非JPG入力ファイルの出力画像全体に対して、全解像度レベルの損失のない LZW 圧縮に使用されます。 ピクセルタイプ、埋め込みカラープロファイル、XMP メタデータなど。 が維持されます。

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
