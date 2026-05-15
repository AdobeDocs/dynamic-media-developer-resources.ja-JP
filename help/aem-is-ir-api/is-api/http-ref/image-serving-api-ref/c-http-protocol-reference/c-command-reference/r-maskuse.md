---
title: maskUse
description: 画像マスクの使用状況。 画像のマスクまたはアルファチャンネルを画像の操作に使用する方法を指定します（例：colorize=）。 エフェクトレイヤーで指定すると、親レイヤーの背景領域または親レイヤー全体の長方形にエフェクトを適用できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e99101a1-1747-454c-b0c0-3af3335c0497
TQID: 'https://experienceleague.adobe.com/swX7HTiWiAhQlPu9f7Qsay2htiJcxnxOCMeu7YlrCm8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 269
ht-degree: 1%

---

# maskUse{#maskuse}

画像マスクの使用状況。 画像のマスクまたはアルファチャンネルを画像の操作に使用する方法を指定します（例：colorize=）。 エフェクトレイヤーで指定すると、親レイヤーの背景領域または親レイヤー全体の長方形にエフェクトを適用できます。

`maskUse=norm|invert|off`

次の表は、レイヤー画像に関連付けられたマスク（アルファチャンネル）の使用状況とタイプに応じた`maskUse=`の効果を示しています。

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>値</b> </th> 
   <th class="entry"> <b> マスクなし</b> </th> 
   <th class="entry"> <b>関連付けられていないアルファ （または個別のマスク画像） </b> </th> 
   <th class="entry"> <b>関連する（事前乗算された）アルファ </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> </span>から<span class="codeph"> </p> </td> 
   <td> <p> 不透明な画像の長方形 </p> </td> 
   <td> <p> 不透明な画像の長方形 </p> </td> 
   <td> <p> べた塗りの黒で塗りつぶされた長方形の上の画像の描画領域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ノルム </span> </p> </td> 
   <td> <p> 不透明な画像の長方形 </p> </td> 
   <td> <p> 画像の前景エリア </p> </td> 
   <td> <p> 画像またはレイヤーの描画領域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">反転</span> </p> </td> 
   <td> <p> 非表示レイヤー </p> </td> 
   <td> <p> 画像の背景色 </p> </td> 
   <td> <p> べた塗りの黒で塗りつぶされた画像またはレイヤーの背景領域 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f36ad1af348e45aeb3eb336544df30b0}

画像またはレイヤー属性： `layer=comp`の場合、レイヤー0に適用されます。 エフェクトレイヤーで指定すると、親レイヤーから継承されたマスクが変更されます。

画像マスクが適用されない場合（`mask=`または`catalog::Mask`で指定）に、テキストまたは単色レイヤーで指定した場合、`maskUse=`の動作は定義されておらず、サポートされていません。

## 初期設定 {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## 例 {#section-daa371e9be5547368ff6772342acba0a}

画像の背景領域を色付けします。画像の前景は、別のマスクイメージで定義されます。 これは、変更されていない画像の場合、カラー化された画像の背景を上にレイヤーすることで実現されます。

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## 関連項目 {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)、[mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
