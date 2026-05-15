---
description: 次のオプションは、周辺光量補正ファイルの処理を制御します。 sourceFileが周辺光量補正でない場合、これらは無視されます。
solution: Experience Manager
title: 周辺光量補正のオプション
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
TQID: 'https://experienceleague.adobe.com/f9Fkiw7Rxx8O0tLFlmnfETYXNNHI7Yui-2t2lNegrIM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 462
ht-degree: 0%

---

# 周辺光量補正のオプション{#options-for-vignettes}

次のオプションは、周辺光量補正ファイルの処理を制御します。 sourceFileが周辺光量補正でない場合、これらは無視されます。

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -contents</span> </p></td> 
  <td class="stentry"> <p>オブジェクト階層を表し、選択したオブジェクト属性を含むXML ファイルを作成します。 ファイルの内容は、<span class="codeph"> req=contents</span> コマンドで返された内容と同じです。 ファイルの名前はソースファイルと同じですが、<span class="filepath"> .xml</span>というサフィックスが付いています。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> – 切り抜き<span class="varname"> x</span><span class="varname"> y</span><span class="varname"> wid</span><span class="varname"> hei</span></span> </p></td> 
  <td class="stentry"> <p>拡大・縮小する前に周辺光量補正を切り抜きます。 </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> y</span></span>は切り抜き長方形の左上隅で、<span class="codeph"><span class="varname"> wid</span>,<span class="varname"> hei</span></span>は切り抜き長方形のサイズです。 値は、ソースビネットの全解像度ビュー画像に対するピクセル座標です。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> – 切り抜き<span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> widn</span><span class="varname"> hein</span></span> </p> </td> 
  <td class="stentry"> <p>拡大・縮小する前に周辺光量補正を切り抜きます。 </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> yn</span></span>は切り抜き長方形の左上隅で、<span class="codeph"><span class="varname"> widn</span>,<span class="varname"> hein</span></span>は切り抜き長方形のサイズです。 値は、ソースビネットのビュー画像に対して正規化され、0.0 ～ 1.0の間である必要があります。 </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> widn</span></span>および<span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> hein</span></span>は1.0以下である必要があります。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -embedmaterials</span> </p></td> 
  <td class="stentry"> <p>出力ビネットに埋め込まれたマテリアルを保持します。 デフォルトでは、マテリアルは出力ビネットから削除されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>1つ以上の出力ビネット高さ（ピクセル単位）。 -infoが指定されている場合は無視されます。 <span class="varname"> ival</span>は0である可能性があります。これは、入力ビネットの幅を示します。 詳しくは、<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> ビネットの拡大・縮小</a>を参照してください。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>周辺光量補正からの画像マップファイルの抽出を有効にします。 マップデータは、<span class="codeph"> &lt;map&gt;</span>要素のみを含むHTML ファイルに書き込まれます。 出力ファイルの名前は、出力画像ファイルと同じですが、<span class="filepath"> .htm</span>という接尾辞が付いています。 警告メッセージが生成され、コマンドを指定しても周辺光量補正にマップデータが存在しない場合はファイルは作成されません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -profile</span> </p></td> 
  <td class="stentry"> <p>ビネットに埋め込まれたICC プロファイルのコピーをファイルに保存します。 警告メッセージが生成され、コマンドを指定してもビネットにICC プロファイルが存在しない場合は、ICC プロファイルファイルは作成されません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> – ピラミッド </span> </p></td> 
  <td class="stentry"> <p>ピラミッド ビネットを作成します。 レンダリングされた画像をDynamic Media ズームビューアで表示する場合に必要です。 詳しくは、<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> ビネットの拡大・縮小</a>を参照してください。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>サムネール画像のピクセル幅と高さの制約。 指定した場合は、ビネット表示画像、キャビネットスタイルファイルのパネル画像、またはウィンドウ被覆用スタイルファイルの最初のスタイルのイルミネーションマップから、幅が広くなく高さ<span class="varname">以下のJPEG画像が生成されます。 </span></p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>1つ以上の出力ビネット幅（ピクセル単位）。 <span class="codeph"> -info</span>が指定されている場合は無視されます。 <span class="varname"> ival</span>は0である可能性があります。これは、入力ビネットの高さを示します。 詳しくは、<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> ビネットの拡大・縮小</a>を参照してください。 </p></td> 
 </tr> 
</table>
