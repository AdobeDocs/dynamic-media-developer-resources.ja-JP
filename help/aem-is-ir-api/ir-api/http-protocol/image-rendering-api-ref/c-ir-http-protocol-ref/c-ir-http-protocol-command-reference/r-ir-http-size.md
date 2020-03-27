---
description: デカールのサイズ デカルの材料のサイズを指定します。
seo-description: デカールのサイズ デカルの材料のサイズを指定します。
seo-title: サイズ
solution: Experience Manager
title: サイズ
topic: Scene7 Image Serving - Image Rendering API
uuid: b82f3429-3d84-4707-8126-d390239df9a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# サイズ{#size}

デカールのサイズ デカルの材料のサイズを指定します。

` size= *`width,height`*[ *`,thickness`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> width, height </span> </p> </td> 
  <td class="stentry"> <p>シーンの座標単位（通常はインチ）（実数、実数）でのデカールオブジェクトのサイズ。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> thickness </span> </p> </td> 
  <td class="stentry"> <p>シーンの座標単位（通常はインチ）でのデカールオブジェクトの厚さ（実数）。 </p> </td> 
 </tr> 
</table>

幅と高さのいずれも0でない場合、画像は指定した寸法に合わせて拡大縮小され、画像の縦横比は保持されません。 いずれかの値を0に設定すると、画像の縦横比が維持されます。

を指定 *`thickness`* すると、ビネットオブジェクトで適切なライトベクトルが定義されている場合は、ドロップシャドウがレンダリングされます。 0に設定 *`thickness`* すると、ドロップシャドウのレンダリングが無効になります。

## プロパティ {#section-818e01e91fed4015951189c818ef28d8}

マテリアル属性。 デカルでのみ使用され、他のすべてのマテリアルでは無視されます。 `res=` の値が0より大きい場合は無視されます。 負の値は指定できません。

## 初期設定 {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` デカル転写材料がカタログエントリに基づく場合、それ以外の場 `size=0,0,0`合は デカル転写のサイズは、が指定されてい `res=` ないか、 *`wid`* 0に設定さ *`hei`* れている場合に、から計算されます。 を指定しない場合、または0に設定した場合、ド *`thickness`* ロップシャドウはレンダリングされません。

## 例 {#section-04fdc2b60b9e4071b672bf6a913738ad}

デカル転写のMSSは、解像度に基づいてサイズが決まり、時計回りに20°回転し、厚さが2.5インチで、ドロップシャドウ効果を適切に適用します。

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## 関連項目 {#section-1b116ecd60214732a1757ee1f0cf21c2}

[シーン座標](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1)、 [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)、 [attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
