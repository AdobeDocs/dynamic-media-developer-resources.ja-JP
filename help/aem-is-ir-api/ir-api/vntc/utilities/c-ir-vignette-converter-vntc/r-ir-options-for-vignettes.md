---
description: 次のオプションは、ビネットファイルの処理を制御します。 sourceFile がビネットでない場合、それらは無視されます。
solution: Experience Manager
title: ビネットのオプション
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# ビネットのオプション{#options-for-vignettes}

次のオプションは、ビネットファイルの処理を制御します。 sourceFile がビネットでない場合、それらは無視されます。

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -contents</span> </p></td> 
  <td class="stentry"> <p>選択したオブジェクト属性を含むオブジェクト階層を表す XML ファイルを作成します。 ファイルの内容は、<span class="codeph"> req=contents</span> コマンドで返される内容と同じです。 ファイルの名前はソースファイルと同じですが、サフィックスは.xml<span class="filepath"></span> す。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-crop <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> wid</span><span class="varname"> hei</span></span> </p></td> 
  <td class="stentry"> <p>拡大縮小する前にビネットを切り抜きます。 </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> y</span></span> は切り抜き長方形の上隅、<span class="codeph"><span class="varname"> wid</span>,<span class="varname"> hei</span></span> は切り抜き長方形のサイズです。 値は、ソースビネットの全解像度ビューイメージを基準としたピクセル座標です。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> widn</span><span class="varname"> hein</span></span> </p> </td> 
  <td class="stentry"> <p>拡大縮小する前にビネットを切り抜きます。 </p> <p>xn<span class="codeph">,<span class="varname"> yn</span><span class="varname"></span></span> <span class="codeph"><span class="varname"> 切り抜き長方形の上隅であり、widn</span>,<span class="varname"> hein</span></span> は切り抜き長方形のサイズです。 値はソース ビネットのビュー画像を基準に正規化され、0.0 ～ 1.0 の範囲でなければなりません。 </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> widn</span></span> と <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> hein</span></span> は 1.0 以下にする必要があります。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -embedmaterials</span> </p></td> 
  <td class="stentry"> <p>埋め込みマテリアルを出力ビネットに保持します。 既定では、マテリアルは出力ビネットから削除されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>1 つ以上の出力ビネットの高さ（ピクセル単位）。 -info が指定されている場合は無視されます。 <span class="varname"> ival</span> は、入力ビネットの幅を表す 0 を指定できます。 詳しくは、<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignette Scaling</a> を参照してください。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>ビネットからの画像マップファイルの抽出を有効にします。 マップデータは、<span class="codeph"> &lt;map&gt;</span> 要素のみを含むHTML ファイルに書き込まれます。 出力ファイルの名前は出力画像ファイルと同じですが、サフィックスは <span class="filepath">.htm</span> です。 コマンドを指定しても、ビネットにマップ データが存在しない場合は、警告メッセージが生成され、ファイルは作成されません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -profile</span> </p></td> 
  <td class="stentry"> <p>ビネットに埋め込まれた ICC プロファイルのコピーをファイルに保存します。 コマンドを指定しても、ビネットに ICC プロファイルが存在しない場合は、警告メッセージが生成され、ICC プロファイルファイルは作成されません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> – ピラミッド </span> </p></td> 
  <td class="stentry"> <p>ピラミッド ビネットを作成します。 レンダリングされた画像を Dynamic Media ズームビューアで表示する場合は必須です。 詳しくは、<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignette Scaling</a> を参照してください。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>サムネール画像のピクセルの幅と高さの制約。 これを指定すると、ビネット ビューのイメージ、キャビネット スタイル ファイルのパネル イメージ <span class="varname"> または窓を覆うスタイル ファイル内の最初のスタイルの照明マップから、幅が </span> ival よりも広くなく、高さが 100% 未満のJPEG イメージが生成されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>ピクセル単位の 1 つ以上の出力ビネット幅。 -info<span class="codeph"> が指定され </span> いる場合は無視されます。 <span class="varname"> ival</span> は、入力ビネットの高さを表す 0 を指定できます。 詳しくは、<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignette Scaling</a> を参照してください。 </p></td> 
 </tr> 
</table>
