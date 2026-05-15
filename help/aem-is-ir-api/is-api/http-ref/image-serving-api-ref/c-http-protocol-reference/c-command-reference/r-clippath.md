---
title: clipPath
description: レイヤークリップパス： 現在のレイヤーのクリップパスを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
TQID: 'https://experienceleague.adobe.com/K4w8R8Ke-0GXFdhfpxgAcltyN3icVsJJdRGfx1OiSjg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 556
ht-degree: 0%

---

# clipPath{#clippath}

レイヤークリップパス： 現在のレイヤーのクリップパスを指定します。

`clipPath= *`pathDefinition`*`

`clipPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>パスデータ： </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>レイヤーソース画像に埋め込まれたパスの名前（ASCIIのみ）。 </p></td> 
 </tr> 
</table>

`clipPath=`で定義された領域の外側にあるレイヤーの部分はすべて透明になります。

`*`pathName`*`は、レイヤーソース画像に埋め込まれたパスの名前です。 パスは、画像コンテンツとの相対的な整合性を維持するために自動的に変換されます。 複数の`*`pathName`*`が指定されている場合、サーバーはこれらのパスの交差点に画像をクリップします。 ソース画像に見つからない`*`pathName`*`はすべて無視されます。

>[!NOTE]
>
>`*`pathName`*`では、ASCII文字列のみがサポートされています。

`*`pathDefinition`*`では、レイヤーのピクセル座標に明示的なパスデータを指定できます。

0,0ではなく`size=`が指定されている場合、レイヤーはプレシズされます。 この場合、パス座標はレイヤー長方形の左上隅を基準とし、レイヤーは`origin=`またはそのデフォルトに基づいて配置されます。 レイヤーの長方形の外側にあるパスの領域は、透明のままです。

単色レイヤーまたはテキストレイヤーに`size=`が指定されていない場合、そのレイヤーは、パスの範囲によってサイズが決まるセルフサイズと見なされます。 `origin=`が指定されていない場合、デフォルトはパス座標空間の（0,0）になります。 このワークフロープロセスにより、レイヤー0の原点に対してパス座標を指定することができます。

>[!NOTE]
>
>単色レイヤーのセルフサイズ設定には、`scale=`、`rotate=`、`anchor=` コマンドは使用できません。

`*`pathDefinition`*`は、SVG `<path>`要素の`d=`属性の値と同様の文字列を受け入れます。ただし、値を区切るスペースの代わりにコンマが使用されます。 `*`pathDefinition`*`には、1つ以上のクローズドループサブパスを含めることができます。

次のパスコマンドは、`*`pathDefinition`*`でサポートされています。

<table id="table_A74DD7A48B1C417D9D4BA46BECEAB981"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> コマンド </b> </th> 
   <th class="entry"> <b>名</b> </th> 
   <th class="entry"> <b>説明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <b> M</b> <span class="varname"> x,y</span> </td> 
   <td> <p> 絶対に移動 </p> </td> 
   <td> <p> x,yで新しいサブパスを開始します。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> m</b> <span class="varname"> x,y</span> </td> 
   <td> <p> 相対に移動 </p> </td> 
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
   <td> <p> curveto absolute </p> </td> 
   <td> <p> 現在の位置からベジェカーブをx,yに描画します。 x1,y1は曲線の先頭の制御点であり、x2,y2は曲線の最後の制御点です。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto relative </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>z</b> </td> 
   <td> <p> closepath </p> </td> 
   <td> <p> 直線で現在のサブパスを閉じます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

大文字のコマンドは、座標の値が（レイヤーの長方形の左上に対して）絶対ピクセル位置にあることを示します。 ピクセルオフセットは、現在の位置に対する小文字のコマンドに従います。

「m」または「M」は、常に新しいサブパスを開始します。 末尾に「Z」または「z」が指定されていない場合、サブパスは自動的に（直線で）閉じられます。

サブパスが相対移動先（「m」）で始まる場合、次のいずれかの相対パスになります。

* 前のサブパスの開始点（ZまたはZで閉じられた場合）。
* 前のサブパスの終了点（明示的に閉じられていない場合）。
* 最初のサブパスである場合は0,0。

## プロパティ {#section-d4127db0dac54e3cbd44f7ea1e001960}

レイヤー属性。 現在のレイヤーまたは`layer=comp`の場合はコンポジット画像に適用されます。 エフェクトレイヤーはそれを無視します。

指定された名前のパスがレイヤーソース画像に見つからない場合、またはレイヤーソースが画像でない場合、修飾子`clipPathE=`は無視されます。

## 初期設定 {#section-076c35ea37fa4a44ada253b4c2dec1dd}

なし（レイヤーの追加クリッピングなし）。

## 関連項目 {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53)、[textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)、[extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
