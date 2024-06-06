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
  <td class="stentry"> <p>選択したオブジェクト属性を含むオブジェクト階層を表す XML ファイルを作成します。 ファイルの内容は、 <span class="codeph"> req=contents</span> コマンド。 ファイルの名前はソースファイルと同じですが、 <span class="filepath"> .xml</span> サフィックス。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-crop <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> wid</span><span class="varname"> ヘイ</span></span> </p></td> 
  <td class="stentry"> <p>拡大縮小する前にビネットを切り抜きます。 </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> y</span></span> は、切り抜き長方形の左上隅です。 <span class="codeph"><span class="varname"> wid</span>,<span class="varname"> ヘイ</span></span> は、切り抜き長方形のサイズです。 値は、ソースビネットの全解像度ビューイメージを基準としたピクセル座標です。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> 幅</span><span class="varname"> ヘイン</span></span> </p> </td> 
  <td class="stentry"> <p>拡大縮小する前にビネットを切り抜きます。 </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> yn</span></span> は、切り抜き長方形の左上隅です。 <span class="codeph"><span class="varname"> 幅</span>,<span class="varname"> ヘイン</span></span> は、切り抜き長方形のサイズです。 値はソース ビネットのビュー画像を基準に正規化され、0.0 ～ 1.0 の範囲でなければなりません。 </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> 幅</span></span> および <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> ヘイン</span></span> は 1.0 以下にする必要があります。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -embedmaterials</span> </p></td> 
  <td class="stentry"> <p>埋め込みマテリアルを出力ビネットに保持します。 既定では、マテリアルは出力ビネットから削除されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> – 高さ <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>1 つ以上の出力ビネットの高さ（ピクセル単位）。 -info が指定されている場合は無視されます。 <span class="varname"> ival</span> 0 を指定すると、入力ビネットの幅を表します。 参照： <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> ビネット拡大縮小</a> を参照してください。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>ビネットからの画像マップファイルの抽出を有効にします。 マップ データは、を含むHTML ファイルにのみ書き込まれます。 <span class="codeph"> &lt;map&gt;</span> 要素。 出力ファイルの名前は出力画像ファイルと同じですが、 <span class="filepath"> .htm</span> サフィックス。 コマンドを指定しても、ビネットにマップ データが存在しない場合は、警告メッセージが生成され、ファイルは作成されません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -profile</span> </p></td> 
  <td class="stentry"> <p>ビネットに埋め込まれた ICC プロファイルのコピーをファイルに保存します。 コマンドを指定しても、ビネットに ICC プロファイルが存在しない場合は、警告メッセージが生成され、ICC プロファイルファイルは作成されません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">  – ピラミッド</span> </p></td> 
  <td class="stentry"> <p>ピラミッド ビネットを作成します。 レンダリング済みの画像をDynamic Media ズームビューアで表示する場合は必須です。 参照： <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> ビネット拡大縮小</a> を参照してください。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>サムネール画像のピクセルの幅と高さの制約。 指定した場合、幅と高さが同じでないJPEG画像 <span class="varname"> ival</span> は、ビネット ビューのイメージ、キャビネット スタイル ファイルのパネル イメージ、または窓被覆スタイル ファイル内の最初のスタイルの照明マップから生成されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>ピクセル単位の 1 つ以上の出力ビネット幅。 次の場合は無視 <span class="codeph"> -info</span> が指定されている。 <span class="varname"> ival</span> 0 を指定すると、入力ビネットの高さを表します。 参照： <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> ビネット拡大縮小</a> を参照してください。 </p></td> 
 </tr> 
</table>
