---
description: デカールのサイズ デカールの材料のサイズを指定します。
seo-description: デカールのサイズ デカールの材料のサイズを指定します。
seo-title: サイズ
solution: Experience Manager
title: サイズ
topic: Scene7 Image Serving - Image Rendering API
uuid: b82f3429-3d84-4707-8126-d390239df9a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 3%

---


# サイズ{#size}

デカールのサイズ デカールの材料のサイズを指定します。

` size= *`width,height`*[ *`,thickness`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> width, height  </span> </p> </td> 
  <td class="stentry"> <p>シーンの座標単位（通常はインチ）でのデカールオブジェクトのサイズ（実数、実数）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 太さ  </span> </p> </td> 
  <td class="stentry"> <p>シーンの座標単位（通常はインチ）でのデカールオブジェクトの厚さ（実数）。 </p> </td> 
 </tr> 
</table>

幅と高さのいずれも0でない場合、画像は指定した寸法に合わせて拡大縮小され、画像の縦横比は維持されません。 いずれかの値を0に設定すると、画像の縦横比が維持されます。

*`thickness`*&#x200B;を指定した場合、ビネットオブジェクトに適切なライトベクトルが定義されていると、ドロップシャドウがレンダリングされます。 ドロップシャドウレンダリングを無効にするには、*`thickness`*&#x200B;を0に設定します。

## プロパティ {#section-818e01e91fed4015951189c818ef28d8}

マテリアル属性 デカルでのみ使用他のすべてのマテリアルでは無視されます。 `res=` は、widthまたはheightが0より大きい場合は無視されます。負の値は指定できません。

## 初期設定 {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` デカル転写のマテリアルがカタログエントリに基づいている場合、それ以外 `size=0,0,0`の場合は、*`wid`*&#x200B;と&#x200B;*`hei`*&#x200B;を指定しない場合、または0に設定されている場合は、`res=`からデカールのサイズが計算されます。 *`thickness`*&#x200B;を指定しない場合、または0に設定した場合、ドロップシャドウはレンダリングされません。

## 例 {#section-04fdc2b60b9e4071b672bf6a913738ad}

デカールのMSSは、解像度に基づいてサイズが決定され、右回りに20度回転し、厚さが2.5インチで、ドロップシャドウ効果を適用します。

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## 関連項目 {#section-1b116ecd60214732a1757ee1f0cf21c2}

[シーン座標](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1)、 [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)、 [attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
