---
title: サイズ
description: デカールのサイズ。 デカール材料のサイズを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 756d8b9f-076a-48d6-95c9-e0d6caeed3dd
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%

---

# サイズ{#size}

デカールのサイズ。 デカール材料のサイズを指定します。

` size= *`width,height`*[ *`，太さ`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 幅、高さ </span> </p> </td> 
  <td class="stentry"> <p>デカールオブジェクトのシーン座標単位（通常はインチ）でのサイズ（実数、実数）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 太さ </span> </p> </td> 
  <td class="stentry"> <p>シーンの座標単位（通常はインチ）（実数）でのデカールオブジェクトの厚さ。 </p> </td> 
 </tr> 
</table>

幅も高さも 0 でない場合、画像は指定されたサイズに合わせて拡大縮小され、画像の縦横比は保持されません。 どちらかの値を 0 に設定すると、画像の縦横比が保持されます。

If *`thickness`* を指定すると、ビネットオブジェクトで適切なライトベクトルが定義されている場合は、ドロップシャドウがレンダリングされます。 設定 *`thickness`* を 0 に設定します。

## プロパティ {#section-818e01e91fed4015951189c818ef28d8}

材料属性。 デカルでのみ使用される。他のすべての材料では無視されます。 `res=` width または height のいずれかが 0 より大きい場合、は無視されます。 負の値にすることはできません。

## 初期設定 {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` デカールのマテリアルがカタログエントリに基づいている場合、そうでない `size=0,0,0`. デカールのサイズは次の値から計算されます。 `res=` if *`wid`* および *`hei`* が指定されていないか、0 に設定されています。 次の場合、ドロップシャドウはレンダリングされません。 *`thickness`* が指定されていないか、0 に設定されています。

## 例 {#section-04fdc2b60b9e4071b672bf6a913738ad}

デカールの MSS は、解像度に基づいてサイズを変更し、時計回りに 20 度回転し、厚さが 2.5 インチで、適切なドロップシャドウ効果を実現します。

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## 関連項目 {#section-1b116ecd60214732a1757ee1f0cf21c2}

[シーン座標](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1), [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04), [attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
