---
title: clipPath
description: レイヤークリップパス。 現在のレイヤーのクリップパスを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# clipPath{#clippath}

レイヤークリップパス。 現在のレイヤーのクリップパスを指定します。

`clipPath= *`pathDefinition`*`

`clipPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>パスデータ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>レイヤーソース画像に埋め込まれたパスの名前（ASCII のみ）。 </p></td> 
 </tr> 
</table>

レイヤーで定義された領域の外側にあるレイヤーの部分 `clipPath=` 透明にレンダリングされます。

`*`pathName`*` は、レイヤーソース画像に埋め込まれたパスの名前です。 パスは、画像のコンテンツとの相対的な整合性を維持するために自動的に変換されます。 複数の `*`pathName`*` が指定されている場合、サーバーは画像をこれらのパスの積集合にクリップします。 ソース画像に見つからない `*`pathName`*` は無視されます。

>[!NOTE]
>
>`*`pathName`*` では ASCII 文字列のみがサポートされています。

`*`pathDefinition`*` レイヤーのピクセル座標に明示的なパスデータを指定できます。

0,0 ではなく `size=` を指定した場合、レイヤーがプレビューされます。 この場合、パス座標はレイヤーの長方形の左上隅を基準とし、レイヤーは `origin=` またはそのデフォルトに基づいて配置されます。 レイヤーの長方形の外側にあるパスの領域は、透明なままです。

単色レイヤーまたはテキストレイヤーに `size=` が指定されていない場合、レイヤーは、パスの範囲がそのサイズを決定するセルフサイズと見なされます。 `origin=` を指定しない場合は、パス座標空間の（0,0）がデフォルトになります。 このワークフロープロセスでは、レイヤー 0 の原点を基準としたパス座標を指定できます。

>[!NOTE]
>
>`scale=`、`rotate=`、`anchor=` のコマンドは、ソリッドカラーレイヤーのサイズを自動調整する場合は使用できません。

`*`pathDefinition`*` SVG `d=` 要素の `<path>` 属性の値と同様の文字列を受け入れます。ただし、値を区切るためにスペースの代わりにコンマが使用される点が異なります。 `*`pathDefinition`*` には、1 つ以上の閉じたループのサブパスを含めることができます。

次のパスコマンドが `*`pathDefinition`*` でサポートされています。

<table id="table_A74DD7A48B1C417D9D4BA46BECEAB981"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> コマンド </b> </th> 
   <th class="entry"> <b> Name</b> </th> 
   <th class="entry"> <b> Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <b> M</b> <span class="varname"> x,y</span> </td> 
   <td> <p> 絶対に移動 </p> </td> 
   <td> <p> x,y で新しいサブパスを開始します。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> m</b> <span class="varname"> x,y</span> </td> 
   <td> <p> 動く親類 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> 絶対ライン </p> </td> 
   <td> <p> 現在の位置から x,y まで線を引きます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto relative </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto absolute </p> </td> 
   <td> <p> 現在の位置から x,y までベジェ曲線を描画します。x1,y1 は曲線の始点のコントロール ポイントで、x2,y2 は曲線の終点のコントロール ポイントです。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto relative </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>z</b> </td> 
   <td> <p> closepath </p> </td> 
   <td> <p> 現在のサブパスを直線で閉じます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

大文字のコマンドは、座標値が（レイヤーの長方形の左上を基準にして）ピクセルの絶対位置にあることを示します。 ピクセルオフセットは、現在の位置を基準にした小文字のコマンドに従います。

「m」または「M」は、常に新しいサブパスを開始します。 終点で「Z」または「z」が指定されていない場合、サブパスは自動的に（直線で）閉じられます。

サブパスが相対移動（&#39;m&#39;）で始まる場合は、次のいずれかに対する相対パスになります。

* 前のサブパスの開始点（「z」または「Z」で閉じられた場合）
* 前のサブパスの終了点（明示的に閉じられていない場合）。
* 0,0 （最初のサブパスの場合）

## プロパティ {#section-d4127db0dac54e3cbd44f7ea1e001960}

レイヤー属性。 現在のレイヤーまたは合成イメージ（`layer=comp` の場合）に適用されます。 エフェクトレイヤーはそれを無視します。

指定した名前のパスがレイヤーソースイメージに見つからない場合、またはレイヤーソースがイメージでない場合、修飾子 `clipPathE=` は無視されます。

## 初期設定 {#section-076c35ea37fa4a44ada253b4c2dec1dd}

なし（レイヤーの追加クリッピングをおこなわない場合）。

## 関連項目 {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) , [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
