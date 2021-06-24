---
description: 画像マスクの使用方法。 画像のマスクまたはアルファチャンネルを画像に対する操作（例えば、colorize=）に使用する方法を指定します。 エフェクトレイヤーで指定すると、親レイヤーの背景領域または親レイヤーの長方形全体に効果を適用できます。
solution: Experience Manager
title: maskUse
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: e99101a1-1747-454c-b0c0-3af3335c0497
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---

# maskUse{#maskuse}

画像マスクの使用方法。 画像のマスクまたはアルファチャンネルを画像に対する操作（例えば、colorize=）に使用する方法を指定します。 エフェクトレイヤーで指定すると、親レイヤーの背景領域または親レイヤーの長方形全体に効果を適用できます。

`maskUse=norm|invert|off`

次の表に、レイヤーイメージに関連付けられたマスク（アルファチャンネル）の使用可否と種類に応じた`maskUse=`の効果を示します。

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
   <td> <p> <span class="codeph"> norm  </span> </p> </td> 
   <td> <p> 不透明な画像の長方形 </p> </td> 
   <td> <p> 画像の前景領域 </p> </td> 
   <td> <p> 画像またはレイヤーの前景領域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 反転  </span> </p> </td> 
   <td> <p> 非表示レイヤー </p> </td> 
   <td> <p> 画像の背景領域 </p> </td> 
   <td> <p> 黒で塗りつぶされた画像またはレイヤーの背景領域 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f36ad1af348e45aeb3eb336544df30b0}

イメージまたはレイヤの属性。 `layer=comp`の場合はレイヤ0に適用されます。 エフェクトレイヤーで指定した場合は、親レイヤーから継承されたマスクが変更されます。

`maskUse=`の動作は未定義で、イメージマスクが適用できない場合はテキストレイヤーまたはソリッドカラーレイヤーで指定されている場合はサポートされません（`mask=`または`catalog::Mask`で指定）。

## 初期設定 {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## 例 {#section-daa371e9be5547368ff6772342acba0a}

画像の背景領域に色を付ける前景画像は、個別のマスク画像で定義されます。 これは、未変更の画像の場合に、色付きの画像の背景を上に重ねることで実現されます。

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## 関連項目 {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) 、 [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
