---
description: 画像マスクの使用 画像のマスクまたはアルファチャンネルを画像の操作（例えば、colorize=）に使用する方法を指定します。 エフェクトレイヤーで指定した場合、親レイヤーの背景領域または親レイヤーの長方形全体にエフェクトを適用できます。
seo-description: 画像マスクの使用 画像のマスクまたはアルファチャンネルを画像の操作（例えば、colorize=）に使用する方法を指定します。 エフェクトレイヤーで指定した場合、親レイヤーの背景領域または親レイヤーの長方形全体にエフェクトを適用できます。
seo-title: maskUse
solution: Experience Manager
title: maskUse
topic: Scene7 Image Serving - Image Rendering API
uuid: 2c70da87-f869-495a-be50-226a4516e002
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# maskUse{#maskuse}

画像マスクの使用 画像のマスクまたはアルファチャンネルを画像の操作（例えば、colorize=）に使用する方法を指定します。 エフェクトレイヤーで指定した場合、親レイヤーの背景領域または親レイヤーの長方形全体にエフェクトを適用できます。

`maskUse=norm|invert|off`

次の表に、レイヤー画像に関連付けら `maskUse=` れているマスク（アルファチャンネル）の可用性と種類に応じたの効果を示します。

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 値</b> </th> 
   <th class="entry"> <b> マスクなし</b> </th> 
   <th class="entry"> <b> 関連付けられていないアルファ（または別のマスク画像）</b> </th> 
   <th class="entry"> <b> 関連付けられた（乗算済み）アルファ</b> </th> 
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
   <td> <p> <span class="codeph"> norm </span> </p> </td> 
   <td> <p> 不透明な画像の長方形 </p> </td> 
   <td> <p> 画像の前景領域 </p> </td> 
   <td> <p> 画像またはレイヤーの前景領域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 反転 </span> </p> </td> 
   <td> <p> 非表示のレイヤー </p> </td> 
   <td> <p> 画像の背景領域 </p> </td> 
   <td> <p> 黒一色で塗りつぶされた画像またはレイヤーの背景領域 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f36ad1af348e45aeb3eb336544df30b0}

画像またはレイヤー属性。 レイヤー0の場合に適用されま `layer=comp`す。 エフェクトレイヤーで指定した場合は、親レイヤーから継承したマスクが変更されます。

の動作は未定義で、 `maskUse=` またはで指定した画像マスクが適用されない場合にテキストまたはべた塗りレイヤーで指定した場合はサポートさ `mask=` れませ `catalog::Mask`ん。

## 初期設定 {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## 例 {#section-daa371e9be5547368ff6772342acba0a}

画像の背景領域に色を付ける画像の前景は、別のマスク画像で定義されます。 これは、未変更の画像の場合に、色付きの画像の背景を上にレイヤー化することで達成できます。

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## 関連項目 {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
