---
title: maskUse
description: 画像マスクの使用。 イメージ上での操作にイメージのマスク チャンネルまたはアルファ チャンネルを使用する方法を指定します（例：colorize=）。 エフェクトレイヤーで指定した場合、エフェクトを親レイヤーの背景領域または親レイヤーの長方形全体に適用できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e99101a1-1747-454c-b0c0-3af3335c0497
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---

# maskUse{#maskuse}

画像マスクの使用。 イメージ上での操作にイメージのマスク チャンネルまたはアルファ チャンネルを使用する方法を指定します（例：colorize=）。 エフェクトレイヤーで指定した場合、エフェクトを親レイヤーの背景領域または親レイヤーの長方形全体に適用できます。

`maskUse=norm|invert|off`

次の表に、レイヤーイメージに関連付けられたマスク（アルファチャンネル）の可用性とタイプに応じた `maskUse=` の効果を示します。

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 値 </b> </th> 
   <th class="entry"> <b> マスクなし </b> </th> 
   <th class="entry"> <b> 関連付けられていないアルファ（または個別のマスクイメージ） </b> </th> 
   <th class="entry"> <b> 関連する（乗算済み）アルファ </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> off </span> </p> </td> 
   <td> <p> 不透明な画像の長方形 </p> </td> 
   <td> <p> 不透明な画像の長方形 </p> </td> 
   <td> <p> 黒色で塗りつぶされた長方形の上の画像の前景領域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 標準 </span> </p> </td> 
   <td> <p> 不透明な画像の長方形 </p> </td> 
   <td> <p> 画像の前景領域 </p> </td> 
   <td> <p> 画像またはレイヤーの前景領域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> invert </span> </p> </td> 
   <td> <p> 非表示レイヤー </p> </td> 
   <td> <p> 画像の背景領域 </p> </td> 
   <td> <p> 画像またはレイヤーの黒ベタ塗りの背景領域 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f36ad1af348e45aeb3eb336544df30b0}

イメージまたはレイヤ アトリビュート。 `layer=comp` の場合はレイヤー 0 に適用されます。 エフェクトレイヤーで指定した場合、コマンドは親レイヤーから継承されたマスクを変更します。

`maskUse=` の動作は未定義であり、イメージマスクを適用できない場合（`mask=` または `catalog::Mask` で指定）、テキストレイヤーまたはソリッドカラーレイヤーで指定した場合はサポートされません。

## 初期設定 {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## 例 {#section-daa371e9be5547368ff6772342acba0a}

画像の背景領域を色付けします。画像の前景は、個別のマスク画像によって定義されます。 これは、変更されていない画像の場合は、カラー化された画像の背景を上にレイヤー化することで実現されます。

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## 関連項目 {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
