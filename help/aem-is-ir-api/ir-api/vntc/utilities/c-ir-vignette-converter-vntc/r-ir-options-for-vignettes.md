---
description: 次のオプションは、ビネットファイルの処理を制御します。 sourceFileがビネットでない場合は無視されます。
seo-description: 次のオプションは、ビネットファイルの処理を制御します。 sourceFileがビネットでない場合は無視されます。
seo-title: ビネットのオプション
solution: Experience Manager
title: ビネットのオプション
topic: Scene7 Image Serving - Image Rendering API
uuid: 0cb40314-07ce-496b-a27b-560d7bb4fa8e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ビネットのオプション{#options-for-vignettes}

次のオプションは、ビネットファイルの処理を制御します。 sourceFileがビネットでない場合は無視されます。

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -内容</span> </p></td> 
  <td class="stentry"> <p>選択したオブジェクト属性を含む、オブジェクト階層を表すXMLファイルを作成します。 ファイルの内容は、 <span class="codeph"> req=contentsコマンドで返される内容と同じです</span> 。 ファイルの名前はソースファイルと同じですが、 <span class="filepath"> .xmlというサフィックスが付きます</span> 。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-crop <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> wid</span><span class="varname"> hei</span></span> </p></td> 
  <td class="stentry"> <p>拡大・縮小する前にビネットを切り抜きます。 </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> yは切り抜き長方形の左上隅、</span></span> wid <span class="codeph"><span class="varname"></span><span class="varname"></span></span> ,heiは切り抜き長方形のサイズです。 値は、ソースビネットの最大解像度ビュー画像を基準とするピクセル座標です。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> widn</span><span class="varname"> hein</span></span> </p> </td> 
  <td class="stentry"> <p>拡大・縮小する前にビネットを切り抜きます。 </p> <p><span class="codeph"><span class="varname"> xn</span>,yn<span class="varname"> は切り抜き用の長方形の左上隅、</span></span> widn <span class="codeph"><span class="varname"></span><span class="varname"></span></span> ,heinは切り抜き用の長方形のサイズです。 値は、ソースビネットのビュー画像を基準に正規化され、0.0 ～ 1.0の範囲で指定する必要があります。 </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> widn</span></span> とyn <span class="codeph"><span class="varname"></span></span><span class="codeph"><span class="varname"> +heinは</span></span> 1.0以下にする必要があります。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -embedmaterials</span> </p></td> 
  <td class="stentry"> <p>出力ビネットに埋め込まれたマテリアルを保持します。 初期設定では、出力ビネットからマテリアルが削除されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>1つ以上の出力ビネットの高さ（ピクセル単位）。 -infoが指定されている場合は無視されます。 <span class="varname"> ivalは</span> 0（入力ビネットの幅を示す）になります。 詳しくは、 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> ビネットの拡大</a> ・縮小を参照してください。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>ビネットからの画像マップファイルの抽出を有効にします。 マップデータは、 <span class="codeph"> &lt;map&gt;要素のみを含むHTMLファイルに書き込まれます</span> 。 出力ファイルの名前は、出力画像ファイルと同じ名前ですが、 <span class="filepath"> .htmというサフィックスが付きます</span> 。 コマンドが指定されていても、ビネットにマップデータが存在しない場合、警告メッセージが生成され、ファイルは作成されません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -プロファイル</span> </p></td> 
  <td class="stentry"> <p>ビネットに埋め込まれたICCプロファイルのコピーをファイルに保存します。 コマンドが指定されているが、ビネットにICCプロファイルが存在しない場合、警告メッセージが生成され、ICCプロファイルファイルは作成されません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">  — ピラミッド</span> </p></td> 
  <td class="stentry"> <p>角錐ビネットを作成します。 レンダリングされた画像をScene7ズームビューアで表示する場合は必須です。 詳しくは、 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> ビネットの拡大</a> ・縮小を参照してください。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>サムネール画像のピクセル幅と高さの制約。 指定した場合、ビネットビュー画像、キャビネットスタイルファイルのパネル画像 <span class="varname"></span> 、またはウィンドウカバリングスタイルファイルの最初のスタイルの照明マップから、幅も高さも幅もivalも高さもないJPEG画像が生成されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>1つ以上の出力ビネットの幅（ピクセル単位）。 -infoが指定され <span class="codeph"> ている場合</span> 、無視されます。 <span class="varname"> ivalは</span> 0（入力ビネットの高さを示す）です。 詳しくは、 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> ビネットの拡大</a> ・縮小を参照してください。 </p></td> 
 </tr> 
</table>

