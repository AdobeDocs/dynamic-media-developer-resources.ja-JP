---
description: 画像変換ユーティリティ。
solution: Experience Manager
title: ic
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ab653aae-532b-4f3d-8541-f6296fbf9172
TQID: 'https://experienceleague.adobe.com/ALpdD-ZyQbjzCD6-sexqaq2gMQZGAZvMd7MqaDC6Gyo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 1258
ht-degree: 1%

---

# ic {#ic}

画像変換ユーティリティ。

`ic`は、画像ファイルを最適化されたピラミッド TIFF形式（PTIFF）に変換するコマンド ライン ツールです。 画像サービングは変換なしで画像を処理できますが、512 x 512 ピクセルを超えるすべての画像をPTIFFに変換することをお勧めします。 この変換により、最適なサーバーパフォーマンスとリソース使用が保証され、応答時間が最小限に抑えられます。

写真コンテンツを含むPTIFF ファイルは、JPEGでエンコードすることをお勧めします（`-jpegcompress`を指定）。 コンピューター生成コンテンツは、可逆圧縮（`-deflatecompress`または`-lzwcompress`）の恩恵を受けることができます。 色変換や画素型変換が必要でない限り、JPEGのソース画像データはデコードせずにPTIFFに転送され、画質の劣化を防ぎます。 この場合、指定された圧縮オプションは、低解像度のピラミッド レベルにのみ適用されます。

大きな画像を変換しない場合は、使用するメモリ量を制御するパラメーターを設定する必要はありません。 ただし、次に示す`-maxmem`設定を使用して、`ic`個のメモリを追加します。 必要なメモリ量を計算するための良い経験則は、画像の幅に画像の高さにチャネル数を掛けることです。 例えば、アルファ値が3のRGB画像の場合は4です。 さらに、チャンネルがコンポーネントごとに8倍ではなく16 ビットの場合、最終的な結果は2倍になります。

## 使用方法 {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]`*`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]`*`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]`*`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i> オプション </i> </span> </span> </p> </td> 
   <td colname="col2"> <p>コマンドオプション（以下を参照）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> <i>sourceFile</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>単一の入力画像ファイル </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span> </span> </p> </td> 
   <td colname="col2"> <p>単一の出力PTIFF ファイル（SourceDirectoryで使用する場合は無効）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>入力画像を含むフォルダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>出力PTIFF ファイルが書き込まれるフォルダー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返品 {#section-36a2dcfa39824d29b69547c432366219}

成功した場合は0です。 エラーが発生した場合、ゼロ以外の値が返され、エラーの詳細が`stderr`に送信されます。

## オプション {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> – 圧縮されていない</span> </p> </td> 
   <td colname="col2"> <p>出力画像を圧縮しないでください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress </span> </p> </td> 
   <td colname="col2"> <p>収縮（zip）圧縮を使用します（デフォルト）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress </span> </p> </td> 
   <td colname="col2"> <p>LZW （Lempel-Ziv-Welch）圧縮を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress </span> </p> </td> 
   <td colname="col2"> <p>JPEGのエンコーディングを利用します。 <span class="codeph"> <span class="varname"> sourceFile </span> </span>にアルファデータが含まれている場合、無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality &lt; <span class="varname">品質</span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>JPEGの画質（0～100、デフォルトは95） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplechrominance </span> </p> </td> 
   <td colname="col2"> <p>JPEGのクロマダウンサンプリングを無効にします（カラーテキストとグラフィックの品質を向上させることができます）。 これは、CMYKまたはグレースケールの出力画像には影響しません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm &lt; <span class="varname">量</span>&gt; &lt; <span class="varname">半径</span>&gt; &lt; <span class="varname">しきい値</span>&gt; &lt; <span class="varname"> モノクロ </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>サブサンプルしたピラミッド レベルにアンシャープマスクを適用します。 詳しくは、<a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a>を参照してください。 （フル解像度の画像には適用されません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath </span> </p> </td> 
   <td colname="col2"> <p>ソースファイル内のクリップパスを使用して、関連するアルファデータを作成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi &lt; <span class="varname"> dpi </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> <span class="varname"> destFile </span> </span>の印刷解像度（dpi）。指定しない場合、<span class="codeph"> srcFile </span>の印刷解像度は<span class="codeph"> <span class="varname"> destFile </span> </span>にコピーされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocrop &lt; <span class="varname"> corner </span>&gt; &lt; <span class="varname"> mode </span>&gt; &lt; <span class="varname">許容値</span>&gt; &lt; <span class="varname"> infoFile </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>切り抜き長方形を計算して、単色の背景を最小限に抑えます。 自動切り抜きアルゴリズムによって画像全体が切り抜かれる場合、切り抜き情報は出力されません。 </p> <p>画像を変換せずに切り抜き長方形を計算するには、<span class="codeph"> – 自動切り抜き</span> （<span class="codeph">なし） – 変換</span> （<span class="codeph">なし） <span class="varname"> destFile （</span> </span>）を指定します。</p>

<p><i><b>corner</b></i> - ul | ur | ll | lr </p>
   <p> シードポイントを使用する画像のコーナーを指定します。 モードが1の場合は無視されます。</p>
   <p><i><b> モード </b></i> - 0 | 1</p>
   <p>指定したコーナーピクセルのカラーに基づいて切り抜くには0に設定します。アルファデータがソースイメージに関連付けられている場合は、事前に乗算されたカラーデータに対して機能します。</p>
   <p>アルファデータに基づいて切り抜く場合は「1」に設定します。角は無視され、0は常にシード値になります。ソースイメージにアルファデータが関連付けられていない場合は切り抜きは適用されません。</p> 
   <p><i><b>許容値</b></i> – 許容値と一致します。 実数値0.0 ～ 1.0。 一致するピクセルコンポーネント値の許容値を指定します。 完全一致の場合は0に設定します。</p>
   <p><i><b>infoFile</b></i> – 切り抜き情報データが書き込まれるXML出力ファイルのパスと名前。</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData </span> </p> </td> 
   <td colname="col2"> <p>利用可能な場合は、XMP メタデータを<span class="codeph"> <span class="varname"> sourceFile </span> </span>から<span class="codeph"> <span class="varname"> destFile </span> </span>まで変更なしでコピーします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile </span> </p> </td> 
   <td colname="col2"> <p> 使用可能な場合は、<span class="codeph"> <span class="varname"> destFile </span> </span>にICC カラープロファイルを埋め込みます（デフォルトではプロファイルが埋め込まれていません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt; <span class="varname"> ファイル </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ICC プロファイルファイルのパスと名前。 <span class="codeph"> <span class="varname"> sourceFile </span> </span>のカラースペースを定義します。このカラースペースはピクセルタイプと一致する必要があります。 プロファイルが<span class="codeph"> <span class="varname"> sourceFile </span> </span>に埋め込まれていない場合にのみ、埋め込まれたプロファイルを上書きするため、指定する必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt; <span class="varname"> ファイル </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ICC プロファイルファイルのパスと名前。 <span class="codeph"> <span class="varname"> destFile </span> </span>のピクセルタイプとカラースペースを定義します。 <span class="codeph"> <span class="varname"> sourceFile </span> </span>に埋め込まれたプロファイルがある場合、または<span class="codeph"> -imageprofile </span>が指定されている場合、ICはこのプロファイルに変換します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptual </span> </p> </td> 
   <td colname="col2"> <p>カラースペース変換のための知覚的レンダーインテント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric </span> </p> </td> 
   <td colname="col2"> <p> カラースペース変換の相対的な色域レンダリングインテント（デフォルト）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimetric </span> </p> </td> 
   <td colname="col2"> <p>カラースペース変換のための絶対的な色域レンダーインテント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation </span> </p> </td> 
   <td colname="col2"> <p>カラースペース変換の彩度レンダリングインテント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation </span> </p> </td> 
   <td colname="col2"> <p>特定のカラーコンバージョンのブラックポイント補正を無効にする </p> <p>デフォルトで有効になっています。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8 </span> </p> </td> 
   <td colname="col2"> <p>カラー変換時のディザリング（エラー拡散）を無効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintainpixeltype </span> </p> </td> 
   <td colname="col2"> <p> CMYKからRGBへの自動変換を無効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress </span> </p> </td> 
   <td colname="col2"> <p>JPEG入力画像のデコードと再エンコードを強制します。 </p> <p> <b>注意：</b>このオプションを適用すると、画質が低下する可能性があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2 </span> </p> </td> 
   <td colname="col2"> <p>標準品質（双線形）リサンプリングフィルターを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8 </span> </p> </td> 
   <td colname="col2"> <p>より高い画質（Lanczos ウィンドウ）のリサンプリングフィルター（デフォルト）を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix </span> </p> </td> 
   <td colname="col2"> <p>高画質（FlashPix）のリサンプリングフィルターを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp </span> </p> </td> 
   <td colname="col2"> <p>Photoshopスタイル 8x8 バイキュービックシャープフィルターを使用したダウンサンプル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> – 使用法</span> </p> </td> 
   <td colname="col2"> <p> 最初のオプションとして指定した場合、無効なオプションが検出された場合は、使用情報の出力を抑制します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> – 上書き</span> </p> </td> 
   <td colname="col2"> <p>既存の<span class="codeph"> <span class="varname"> destFile </span> </span>の上書きを許可します。 デフォルトでは、ファイル名に数値サフィックスが追加され、上書きができなくなります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> – 非表示</span>をスキップ </p> </td> 
   <td colname="col2"> <p>非表示のソースファイルを無視します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror </span> </p> </td> 
   <td colname="col2"> <p>エラーが発生したときに処理を停止しないでください。 複数のファイルを処理する場合にのみ効果があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile &lt; <span class="varname"> ファイル </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ログファイルのパスと名前（デフォルトは<span class="codeph"> stdout </span>）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel &lt; <span class="varname"> level </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ログレベル： </p> 
   <p>&lt; 0 - ログ記録が無効です。</p>
   <p>0 – 処理するファイルを一覧表示します。</p>
   <p>1 – 不要なファイルのレポートを追加します。</p>
   <p>2 – 進行状況レポートを追加します。</p>
   <p>3 – 発生したすべてのファイルに関するレポートを追加します。</p>
   <p>4 - ファイルレベルで進行状況レポートを追加します。</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend </span> </p> </td> 
   <td colname="col2"> <p>ログファイルに追加（デフォルト）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend </span> </p> </td> 
   <td colname="col2"> <p>ログファイルを上書きします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogressmsec &lt; <span class="varname"> ミリ秒</span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ログレベル 2以降のログ間隔（ミリ秒単位）（デフォルトは3000）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem &lt; <span class="varname"> バイト </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>メモリ使用量の制限。 少なくとも10 MBである必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent &lt; <span class="varname"> パーセント </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>メモリ使用量の制限。 デフォルトは物理メモリの25%です。 <span class="codeph"> maxmem </span>も<span class="codeph"> maxmempercent </span>も明示的に設定されていない場合は、maxmempercentのデフォルトを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> – バージョン </span> </p> </td> 
   <td colname="col2"> <p> このユーティリティのバージョン情報を返します。 他のオプションなしで指定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## サポートされる入力画像形式 {#section-ab13d941d6724e65b9f84b62d949d31c}

次の表に、ICでサポートされている画像ファイル形式と形式オプションを示します。

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b>形式</b> </p> </th> 
   <th class="entry"> <p> <b> ピクセルの種類</b> <b> ビット/チャン </b> </p> </th> 
   <th class="entry"> <p> <b> ビット/チャン </b> </p> </th> 
   <th class="entry"> <p> <b>圧縮</b> </p> </th> 
   <th class="entry"> <p> <b>件のメモ </b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> （Windows ビットマップ） </p> </td> 
   <td> <p> RGB | インデックス </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> 非圧縮| RLE </p> </td> 
   <td> <p> 5/6 ビット/チャンネルは、16 ビット RGB（5-5-5および5-6-5 ビット/チャンネル）のサポートを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> （カプセル化されたPostscript） </p> </td> 
   <td> <p> CMYK | RGB | グレー </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII | ASCII85 | バイナリ | JPEG </p> </td> 
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
   <td> <p> 存在する場合、パレットの透明度の値はアルファに変換されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG</b> <p> （JFIF/JPEG） </p> </td> 
   <td> <p> CMYK | RGB | グレー </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | グレー| グレー </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 非圧縮|圧縮 </p> </td> 
   <td> <p> 結合された画像のみ。レイヤーと追加チャンネルは無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Mac OS </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RLE </p> </td> 
   <td> <p> ビットマップデータのみ。ベクターデータは無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB | RGBA | グレー| グレーA | インデックス </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> 圧縮 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | グレー| グレーA | インデックス付き </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 非圧縮| ZIP | LZW | JPEG | CCITT RLE | CCITT G3 | CCITT G4 | Packbits </p> </td> 
   <td> <p> 最初に関連付けられたアルファチャンネルを除き、追加のチャンネルは無視されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

埋め込まれたICC プロファイルは、EPS、JPG、PSD、PNG、およびTIFF ファイルで認識されます。

埋め込みパスとXMP メタデータは、EPS、JPG、PSD、およびTIFF ファイルで認識されます。

## 例 {#section-3c1986b30315431989bd76b1ee5bef6d}

単一の画像を最高画質で変換し、同じフォルダーに保存します。

`ic -convert src/myFile.png src/myFile.tif`

*`srcFolder`*&#x200B;のすべての画像をJPEGでエンコードされたピラミッド TIFFに変換し、*`destFolder`*&#x200B;に配置します。

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

*`srcFolder`*&#x200B;のすべての画像を変換します。 JPGファイルのエンコードされた画像データは、これらの画像の残りのピラミッドと、JPG以外のすべての入力ファイルの出力画像全体に対して、完全な解像度レベルのロスレス LZW圧縮に使用されます。 ピクセルタイプ、埋め込みカラープロファイル、XMP メタデータなど。 は維持されます。

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
