---
description: 画像マスクの使用 画像のマスクまたはアルファチャネルを画像の操作に使用する方法（例えば、colorize=）を指定します。 エフェクトレイヤーで指定した場合は、親レイヤーの背景領域または親レイヤーの長方形全体にエフェクトを適用できます。
seo-description: 画像マスクの使用 画像のマスクまたはアルファチャネルを画像の操作に使用する方法（例えば、colorize=）を指定します。 エフェクトレイヤーで指定した場合は、親レイヤーの背景領域または親レイヤーの長方形全体にエフェクトを適用できます。
seo-title: maskUse
solution: Experience Manager
title: maskUse
topic: Scene7 Image Serving - Image Rendering API
uuid: 2c70da87-f869-495a-be50-226a4516e002
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 2%

---


# maskUse{#maskuse}

画像マスクの使用 画像のマスクまたはアルファチャネルを画像の操作に使用する方法（例えば、colorize=）を指定します。 エフェクトレイヤーで指定した場合は、親レイヤーの背景領域または親レイヤーの長方形全体にエフェクトを適用できます。

`maskUse=norm|invert|off`

次の表に、レイヤー画像に関連付けられたマスク(アルファチャネル)の可用性と種類に応じた`maskUse=`の効果を示します。

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 値</b> </th> 
   <th class="entry"> <b> マスクなし</b> </th> 
   <th class="entry"> <b> 関連付けられていないアルファ（または個別のマスク画像）</b> </th> 
   <th class="entry"> <b> 関連付けられた（乗算前の）アルファ</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> オフ </span> </p> </td> 
   <td> <p> 不透明な画像の長方形 </p> </td> 
   <td> <p> 不透明な画像の長方形 </p> </td> 
   <td> <p> 黒一色で塗りつぶされた長方形の上の画像の前景領域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> norm  </span> </p> </td> 
   <td> <p> 不透明な画像の長方形 </p> </td> 
   <td> <p> 画像の前景領域 </p> </td> 
   <td> <p> 画像またはレイヤーの前景領域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 反転  </span> </p> </td> 
   <td> <p> 非表示のレイヤー </p> </td> 
   <td> <p> 画像の背景領域 </p> </td> 
   <td> <p> 黒一色で塗りつぶされた画像またはレイヤーの背景領域 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f36ad1af348e45aeb3eb336544df30b0}

画像またはレイヤーの属性。 `layer=comp`の場合にレイヤー0に適用されます。 エフェクトレイヤーで指定した場合は、親レイヤーから継承したマスクが変更されます。

`maskUse=`の動作は未定義で、画像マスクを適用できない場合はテキストレイヤーまたはべた塗りレイヤーで指定した場合はサポートされません（`mask=`または`catalog::Mask`で指定）。

## 初期設定 {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## 例 {#section-daa371e9be5547368ff6772342acba0a}

画像の背景領域の色彩の統一、画像の前景は、別のマスク画像によって定義されます。 これは、未変更の画像の場合に、カラー化された画像の背景を上にレイヤー化することで達成できます。

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## 関連項目 {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) 、 [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
