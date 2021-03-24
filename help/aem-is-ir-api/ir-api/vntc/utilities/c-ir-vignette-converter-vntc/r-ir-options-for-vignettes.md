---
description: 次のオプションは、ビネットファイルの処理を制御します。 sourceFileがビネットでない場合、これらは無視されます。
solution: Experience Manager
title: ビネットのオプション
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---


# ビネットのオプション{#options-for-vignettes}

次のオプションは、ビネットファイルの処理を制御します。 sourceFileがビネットでない場合、これらは無視されます。

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -内容</span> </p></td> 
  <td class="stentry"> <p>選択したオブジェクト属性を含む、オブジェクト階層を表すXMLファイルを作成します。 ファイルの内容は、<span class="codeph"> req=contents</span>コマンドが返す内容と同じです。 ファイルの名前はソースファイルと同じですが、<span class="filepath"> .xml</span>サフィックスが付きます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-crop  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xywidhei</span></span> </p></td> 
  <td class="stentry"> <p>拡大・縮小する前にビネットを切り抜きます。 </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> </span></span> yは切り抜き長方形の左上隅で、 <span class="codeph"><span class="varname"> wid</span>,<span class="varname"> </span></span> heieは切り抜き長方形のサイズです。値は、ソースビネットの最大解像度表示画像を基準とするピクセル座標です。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xnynwidhein</span></span> </p> </td> 
  <td class="stentry"> <p>拡大・縮小する前にビネットを切り抜きます。 </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> </span></span> ynは切り抜き長方形の左上隅で、 <span class="codeph"><span class="varname"> widn</span>,<span class="varname"> </span></span> heinは切り抜き長方形のサイズです。値は、ソースビネットの表示画像を基準にして正規化され、0.0 ～ 1.0の範囲で設定する必要があります。 </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> </span></span> widnand  <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> </span></span> heinは1.0以下にする必要があります。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -embedmaterials</span> </p></td> 
  <td class="stentry"> <p>出力ビネットに埋め込まれたマテリアルを保持します。 初期設定では、出力ビネットからマテリアルが削除されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>1つ以上の出力ビネットの高さ（ピクセル単位）。 -infoが指定されている場合は無視されます。 <span class="varname"> </span> ivalは0で、入力ビネットの幅を示します。詳しくは、<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local">ビネットの拡大/縮小</a>を参照してください。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>ビネットからの画像マップファイルの抽出を有効化 マップデータは、<span class="codeph"> &lt;map&gt;</span>要素のみを含むHTMLファイルに書き込まれます。 出力ファイルの名前は、出力画像ファイルと同じ名前になりますが、<span class="filepath"> .htm</span>サフィックスが付きます。 警告メッセージが生成され、コマンドが指定されてもビネットにマップデータがない場合、ファイルは作成されません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -プロファイル</span> </p></td> 
  <td class="stentry"> <p>ビネットに埋め込まれたICCプロファイルのコピーをファイルに保存します。 警告メッセージが生成され、コマンドが指定されているがビネットにICCプロファイルがない場合、ICCプロファイルファイルは作成されません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> ピラミッド</span> </p></td> 
  <td class="stentry"> <p>ピラミッドビネットを作成します。 Dynamic Mediaズームビューアでレンダリングした画像を表示する場合は必須です。 詳しくは、<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local">ビネットの拡大/縮小</a>を参照してください。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>サムネール画像のピクセル幅と高さの制約事項。 指定した場合、ビネット表示画像、キャビネットスタイルファイルのパネル画像、またはウィンドウカバリングスタイルファイル内の最初のスタイルの照明マップから、幅も高さも<span class="varname"> ival</span>以下のJPEG画像が生成されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width  <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>1つ以上の出力ビネットの幅（ピクセル単位）。 <span class="codeph"> -info</span>を指定した場合は無視されます。 <span class="varname"> </span> ivalは0で、入力ビネットの高さを示します。詳しくは、<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local">ビネットの拡大/縮小</a>を参照してください。 </p></td> 
 </tr> 
</table>

