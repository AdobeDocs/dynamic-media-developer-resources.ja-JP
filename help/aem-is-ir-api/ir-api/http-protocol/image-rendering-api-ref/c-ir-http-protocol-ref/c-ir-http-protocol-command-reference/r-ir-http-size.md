---
description: デカルのサイズ デカル転写材のサイズを指定します。
solution: Experience Manager
title: サイズ
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 756d8b9f-076a-48d6-95c9-e0d6caeed3dd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 3%

---

# サイズ{#size}

デカルのサイズ デカル転写材のサイズを指定します。

` size= *`width,height`*[ *`,thickness`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 幅、高さ  </span> </p> </td> 
  <td class="stentry"> <p>シーンの座標単位（通常はインチ）（実数、実数）でのデカールオブジェクトのサイズ。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 太さ  </span> </p> </td> 
  <td class="stentry"> <p>シーンの座標単位（通常はインチ）でのデカルオブジェクトの厚さ（実数）。 </p> </td> 
 </tr> 
</table>

幅も高さも0でない場合、画像は指定されたサイズに合わせて拡大縮小され、画像の縦横比は維持されません。 いずれかの値を0に設定すると、画像の縦横比が維持されます。

*`thickness`*&#x200B;を指定した場合、ビネットオブジェクトが適切なライトベクトルを定義すると、ドロップシャドウがレンダリングされます。 ドロップシャドウレンダリングを無効にするには、 *`thickness`*&#x200B;を0に設定します。

## プロパティ {#section-818e01e91fed4015951189c818ef28d8}

マテリアル属性。 デカルでのみ使用他のすべてのマテリアルでは無視されます。 `res=` widthまたはheightのいずれかが0より大きい場合、は無視されます。負の値は指定できません。

## 初期設定 {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` デカル転写のマテリアルがカタログエントリに基づいている場合、それ以外の場合 `size=0,0,0`は。*`wid`*&#x200B;と&#x200B;*`hei`*&#x200B;が指定されていない場合、または0に設定されている場合、デカールのサイズは`res=`から計算されます。 *`thickness`*&#x200B;を指定しない場合や0に設定した場合、ドロップシャドウはレンダリングされません。

## 例 {#section-04fdc2b60b9e4071b672bf6a913738ad}

解像度に基づいてサイズが変更され、時計回りに20度回転し、厚さが2.5インチのデカールのMSSは、適切なドロップシャドウ効果を実現します。

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## 関連項目 {#section-1b116ecd60214732a1757ee1f0cf21c2}

[シーン座標](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1)、 [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)、 [attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
