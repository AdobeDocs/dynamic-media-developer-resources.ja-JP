---
description: レイヤークリップパス 現在の画層のクリップパスを指定します。
solution: Experience Manager
title: clipPath
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 1%

---

# clipPath{#clippath}

レイヤークリップパス 現在の画層のクリップパスを指定します。

`clipPath= *`pathDefinition`*`

`clipPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>レイヤーソース画像に埋め込まれたパスの名前（ASCIIのみ）。 </p></td> 
 </tr> 
</table>

`clipPath=`で定義された領域の外側にあるレイヤーの部分はすべて透明にレンダリングされます。

`*``*` pathNameは、レイヤーソース画像に埋め込まれたパスの名前です。パスは、画像コンテンツとの相対的な整列を維持するために、自動的に変換されます。 複数の`*`pathName`*`を指定した場合、サーバはイメージをこれらのパスの交差点にクリップします。 ソース画像内で`*`pathName`*`が見つからない場合は無視されます。

>[!NOTE]
>
>`*`pathName`*`では、ASCII文字列のみがサポートされています。

`*``*` pathDefinitionを使用すると、レイヤーのピクセル座標に明示的なパスデータを指定できます。

`size=`を指定し、0,0ではない場合は、レイヤーのサイズが事前に設定されます。 この場合、パス座標はレイヤーの長方形の左上隅を基準にして配置され、レイヤーは`origin=`またはデフォルトを基準に配置されます。 レイヤーの長方形の外側のパスの領域は透明のままです。

べた塗りのカラーまたはテキストレイヤーに`size=`を指定しない場合、そのレイヤーは、パスのサイズを決定する範囲での自己サイズ調整と見なされます。 `origin=`を指定しない場合、パス座標空間の(0,0)がデフォルトになります。 これにより、レイヤ0の原点を基準にパス座標を指定できます。

>[!NOTE]
>
>`scale=`、 、お `rotate=`よびコマンドは、 `anchor=` ソリッドカラーレイヤーのセルフサイズ設定には使用できません。

`*``*` pathDefinitionは、SVG要素の属性の値に類似した文字列を受け取りま `d=` す `<path>` が、値を区切るためにスペースの代わりにコンマが使用される点が異なります。`*``*` pathDefinitionには、1つ以上のクローズドループサブパスを含めることができます。

`*`pathDefinition`*`では、次のパスコマンドがサポートされています。

<table id="table_A74DD7A48B1C417D9D4BA46BECEAB981"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> コマンド</b> </th> 
   <th class="entry"> <b> 名前</b> </th> 
   <th class="entry"> <b> 説明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <b> </b> <span class="varname"> Mx,y</span> </td> 
   <td> <p> moveto absolute </p> </td> 
   <td> <p> x,yで新しいサブパスを開始します。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> </b> <span class="varname"> mx,y</span> </td> 
   <td> <p> moveto relative </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto absolute </p> </td> 
   <td> <p> 現在の位置からx,yの間に線を描きます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b>  *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto relative </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> 絶対的な </p> </td> 
   <td> <p> 現在の位置からx,yまでのベジェ曲線を描きます。x1,y1は曲線の始点の制御点で、x2,y2は曲線の終点の制御点です。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b>  *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto relative </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b>  |  <b>z</b> </td> 
   <td> <p> closepath </p> </td> 
   <td> <p> 現在のサブパスを直線で閉じます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

大文字のコマンドは、座標値が絶対ピクセル位置（レイヤーの長方形の左上を基準とする位置）にあることを示します。 ピクセルオフセットは、現在の位置に対する小文字のコマンドに従います。

&#39;m&#39;または&#39;M&#39;は常に新しいサブパスを開始します。 「Z」または「z」が最後に指定されていない場合、サブパスは自動的に（直線で）閉じます。

サブパスが相対移動(&#39;m&#39;)で始まる場合、次のいずれかに対する相対パスになります。

* 前のサブパスの始点（「z」または「Z」で閉じた場合）。
* 前のサブパスの終点（明示的に閉じられなかった場合）。
* 0,0（これが最初のサブパスの場合）

## プロパティ {#section-d4127db0dac54e3cbd44f7ea1e001960}

レイヤー属性。 `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。 エフェクトレイヤーでは無視されます。

`clipPathE=` は、指定した名前のパスがレイヤーソース画像内に見つからない場合、またはレイヤーソースがイメージでない場合は無視されます。

## 初期設定 {#section-076c35ea37fa4a44ada253b4c2dec1dd}

なし（レイヤーの追加のクリップなし）。

## 関連項目 {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) 、  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) 、  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
