---
description: レイヤークリップパス 現在のレイヤーのクリップパスを指定します。
seo-description: レイヤークリップパス 現在のレイヤーのクリップパスを指定します。
seo-title: clipPath
solution: Experience Manager
title: clipPath
topic: Scene7 Image Serving - Image Rendering API
uuid: fe84cf7a-63af-47d3-ae4f-2122f2f0a262
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# clipPath{#clippath}

レイヤークリップパス 現在のレイヤーのクリップパスを指定します。

`clipPath= *`pathDefinition`*`

`clipPathE= *`pathNamepathName`*&#42;[, *``*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span></span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> パス <span class="varname"> 名</span></span> </p> </td> 
  <td class="stentry"> <p>レイヤーソース画像に埋め込まれたパスの名前（ASCIIのみ）。 </p></td> 
 </tr> 
</table>

で定義された領域の外側にあるレイヤーの部分は、透明にレンダ `clipPath=` リングされます。

` *`pathNameは`*` 、レイヤーソース画像に埋め込まれたパスの名前です。 パスは、画像コンテンツとの相対的な位置揃えを維持するように、自動的に変換されます。 複数のpathNameを指定した ` *`場合`*` 、サーバは画像をこれらのパスの交差点にクリップします。 ソー ` *`ス画像で`*` pathNameが見つからない場合は無視されます。

>[!NOTE]
>
>pathNameにはASCII文字列のみがサポートさ ` *`れます`*`。

` *`pathDefinitionを使用すると`*` 、レイヤーのピクセル座標に明示的なパスデータを指定できます。

を指定 `size=` し、0,0以外の場合は、レイヤーのサイズが事前設定されます。 この場合、パスの座標はレイヤーの長方形の左上隅を基準とした相対座標で、レイヤーはデフォルトを基準にし `origin=` て配置されます。 パスのレイヤーの長方形の外側の領域はすべて透明のままです。

べた塗 `size=` りまたはテキストレイヤーに対してを指定しない場合、レイヤーはパスの大きさに応じて自己サイズ調整されたものとみなされます。 を指 `origin=` 定しない場合、パス座標空間の(0,0)がデフォルトになります。 これにより、レイヤー0の原点を基準としたパス座標を効果的に指定できます。

>[!NOTE]
>
>`scale=`、およ `rotate=`びコマ `anchor=` ンドは、ソリッドカラーレイヤーの自動サイズ調整には使用できません。

` *`pathDefinitionは`*` 、SVG要素の属性の値に類似した文字 `d=``<path>` 列を受け取ります。ただし、値を区切る際にスペースの代わりにコンマが使用されます。 ` *`pathDefinitionには`*` 、1つ以上の閉じたループサブパスを含めることができます。

pathDefinitionでは、次のパスコマンドがサポートさ ` *`れます`*`。

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
   <td> <b> M</b><span class="varname"> x,y</span> </td> 
   <td> <p> 絶対移動 </p> </td> 
   <td> <p> x,yで新しいサブパスを開始します。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> m</b><span class="varname"> x,y</span> </td> 
   <td> <p> moveto relative </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto absolute </p> </td> 
   <td> <p> 現在の位置からx,yに線を引きます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto relative </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> 絶対曲線 </p> </td> 
   <td> <p> 現在の位置からx,yにベジェ曲線を描画します。x1,y1はカーブの始点の制御点、x2,y2はカーブの終点の制御点です。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> 親類に </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>z</b> </td> 
   <td> <p> closepath </p> </td> 
   <td> <p> 現在のサブパスを直線で閉じます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

大文字のコマンドは、座標値が（レイヤーの長方形の左上を基準とした）絶対ピクセル位置にあることを示します。 ピクセルオフセットは、現在の位置を基準とする小文字のコマンドに従います。

&#39;m&#39;または&#39;M&#39;は常に新しいサブパスを開始します。 「Z」または「z」が末尾に指定されていない場合、サブパスは（直線で）自動的に閉じられます。

サブパスが相対moveto (&#39;m&#39;)で始まる場合、次のいずれかに対する相対パスになります。

* 前のサブパスが「z」または「Z」で閉じられていた場合の開始点。
* 前のサブパスの終点（明示的に閉じられていない場合）。
* 0,0（最初のサブパスの場合）。

## プロパティ {#section-d4127db0dac54e3cbd44f7ea1e001960}

レイヤー属性。 現在のレイヤーまたは合成画像（の場合）に適用されま `layer=comp`す。 エフェクトレイヤーでは無視されます。

`clipPathE=` が無視されるのは、指定した名前のパスがレイヤーソース画像内に見つからない場合、またはレイヤーソースが画像でない場合です。

## 初期設定 {#section-076c35ea37fa4a44ada253b4c2dec1dd}

なし（レイヤーの追加のクリップなし）。

## 関連項目 {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) , [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
