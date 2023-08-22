---
title: maskUse
description: 画像マスクの使用方法。 画像のマスクまたはアルファチャンネルを画像に対する操作に使用する方法を指定します（例：colorize=）。 エフェクトレイヤーで指定すると、親レイヤーの背景領域または親レイヤーの長方形全体に効果を適用できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e99101a1-1747-454c-b0c0-3af3335c0497
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 2%

---

# maskUse{#maskuse}

画像マスクの使用方法。 画像のマスクまたはアルファチャンネルを画像に対する操作に使用する方法を指定します（例：colorize=）。 エフェクトレイヤーで指定すると、親レイヤーの背景領域または親レイヤーの長方形全体に効果を適用できます。

`maskUse=norm|invert|off`

次の表に、 `maskUse=` レイヤーイメージに関連付けられているマスク（アルファチャンネル）の使用可否と種類に応じて異なります。

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 値</b> </th> 
   <th class="entry"> <b> マスクなし</b> </th> 
   <th class="entry"> <b> 関連付けられていないアルファ（または別のマスク画像）</b> </th> 
   <th class="entry"> <b> 関連（プリマルチプライ）アルファ</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> オフ </span> </p> </td> 
   <td> <p> 不透明な画像の長方形 </p> </td> 
   <td> <p> 不透明な画像の長方形 </p> </td> 
   <td> <p> 黒で塗りつぶされた長方形の上の画像の前景領域 </p> </td> 
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
   <td> <p> 黒で塗りつぶされた画像またはレイヤーの背景領域 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f36ad1af348e45aeb3eb336544df30b0}

画像またはレイヤの属性。 次の場合にレイヤー 0 に適用 `layer=comp`. エフェクトレイヤーで指定した場合は、親レイヤーから継承されたマスクが変更されます。

の動作 `maskUse=` 画像マスクが適用されない場合（で指定される場合）、テキストレイヤーまたはソリッドカラーレイヤーで指定された場合、は未定義でサポートされません。 `mask=` または `catalog::Mask`) をクリックします。

## 初期設定 {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## 例 {#section-daa371e9be5547368ff6772342acba0a}

画像の背景領域に色を付けます。画像の前景は別のマスク画像で定義されます。 これは、未変更の画像の場合に、色付きの画像の背景を上にレイヤーしておくことで実現します。

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## 関連項目 {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
