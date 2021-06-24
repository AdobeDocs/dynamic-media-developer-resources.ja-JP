---
description: 次のオプションは、ビネットファイルの処理を制御します。 sourceFileがビネットでない場合は無視されます。
solution: Experience Manager
title: ビネットのオプション
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 0%

---

# ビネットのオプション{#options-for-vignettes}

次のオプションは、ビネットファイルの処理を制御します。 sourceFileがビネットでない場合は無視されます。

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -内容</span> </p></td> 
  <td class="stentry"> <p>オブジェクト階層を表すXMLファイルを作成し、選択したオブジェクト属性を含めます。 ファイルの内容は、 <span class="codeph"> req=contents</span>コマンドで返される内容と同じです。 ファイルの名前はソースファイルと同じですが、サフィックスは<span class="filepath"> .xml</span>です。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-crop  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xywidhei</span></span> </p></td> 
  <td class="stentry"> <p>拡大縮小する前にビネットを切り抜きます。 </p> <p><span class="codeph"><span class="varname"> x</span>、<span class="varname"> </span></span> は切り抜きの長方形の左上隅、 <span class="codeph"><span class="varname"> wid</span>、<span class="varname"> </span></span> は切り抜きの長方形のサイズです。値は、ソースビネットの最大解像度ビュー画像を基準とするピクセル座標です。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xnynwidhein</span></span> </p> </td> 
  <td class="stentry"> <p>拡大縮小する前にビネットを切り抜きます。 </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> </span></span> ynは切り抜きの長方形の左上隅、 <span class="codeph"><span class="varname"> widn</span>,<span class="varname"> </span></span> heinは切り抜きの長方形のサイズです。値は、ソースビネットのビネットのビュー画像を基準に正規化され、0.0 ～ 1.0の範囲で指定する必要があります。 </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> </span></span> widnand  <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> </span></span>  heinは1.0以下にする必要があります。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -embedmaterials</span> </p></td> 
  <td class="stentry"> <p>出力ビネットに埋め込まれたマテリアルを保持します。 デフォルトでは、出力ビネットからマテリアルが削除されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>1つ以上の出力ビネットの高さ（ピクセル単位）。 -infoが指定されている場合は無視されます。 <span class="varname"> </span> ivalmayは、入力ビネットの幅を示す0です。詳しくは、 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local">ビネットスケーリング</a>を参照してください。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>ビネットからの画像マップファイルの抽出を有効にします。 マップデータは、<span class="codeph"> &lt;map&gt;</span>要素のみを含むHTMLファイルに書き込まれます。 出力ファイルの名前は、出力画像ファイルと同じですが、サフィックスは<span class="filepath"> .htm</span>です。 警告メッセージが生成され、コマンドが指定されてもビネットにマップデータが存在しない場合は、ファイルは作成されません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -プロファイル</span> </p></td> 
  <td class="stentry"> <p>ビネットに埋め込まれたICCプロファイルのコピーをファイルに保存します。 警告メッセージが生成され、コマンドが指定されていても、ビネットにICCプロファイルが存在しない場合、ICCプロファイルファイルは作成されません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">  — ピラミッド</span> </p></td> 
  <td class="stentry"> <p>ピラミッドビネットを作成します。 Dynamic Mediaズームビューアでレンダリングされた画像を表示する場合は必須です。 詳しくは、 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local">ビネットスケーリング</a>を参照してください。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>サムネール画像のピクセル幅と高さの制限。 指定した場合、ビネットビュー画像、キャビネットスタイルファイルのパネル画像、または窓カバースタイルファイル内の第1スタイルの照明マップから、幅が小さく<span class="varname"> ival</span>以下のJPEG画像を生成する。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width  <span class="varname"> ival</span>  *[, <span class="varname"> ival</span> ]</span> </p></td> 
  <td class="stentry"> <p>1つ以上の出力ビネットの幅（ピクセル単位）。 <span class="codeph"> -info</span>が指定されている場合は無視されます。 <span class="varname"> </span> ivalmayは、入力ビネットの高さを示す0です。詳しくは、 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local">ビネットスケーリング</a>を参照してください。 </p></td> 
 </tr> 
</table>
