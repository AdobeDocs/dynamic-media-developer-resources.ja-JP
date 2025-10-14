---
title: サイズ
description: デカル転写サイズ。 デカール マテリアルのサイズを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 756d8b9f-076a-48d6-95c9-e0d6caeed3dd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 2%

---

# サイズ{#size}

デカル転写サイズ。 デカール マテリアルのサイズを指定します。

` size= *`width,height`*[ *`,thickness`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> 幅 <span class="varname"> 高さ </span> </p> </td> 
  <td class="stentry"> <p>デカル転写オブジェクトのサイズをシーン座標単位（通常はインチ）で表示します（実際のサイズ、実際のサイズ）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 厚 </span> </p> </td> 
  <td class="stentry"> <p>デカル転写オブジェクトの厚さ（シーン座標単位（通常はインチ）（実数））。 </p> </td> 
 </tr> 
</table>

幅も高さも 0 でない場合、画像は指定された正確な寸法に拡大/縮小され、画像の縦横比は保持されません。 いずれかの値を 0 に設定すると、画像の縦横比が保持されます。

*`thickness`* を指定すると、ビネット オブジェクトに適切なライト ベクトルが定義されている場合にドロップ シャドウがレンダリングされます。 ドロップシャドウレンダリングを無効にするには、*`thickness`* を 0 に設定します。

## プロパティ {#section-818e01e91fed4015951189c818ef28d8}

マテリアル アトリビュート。 デカル転写でのみ使用されます。他のすべてのマテリアルでは無視されます。 幅または高さが 0 より大きい場合、`res=` は無視されます。 値は負の値にはできません。

## 初期設定 {#section-f91f516c6af54f0eb4d8c964b923cae0}

デカル転写マテリアルがカタログ エントリに基づいている場合は `catalog::Size`、それ以外の場合は `size=0,0,0` です。 `res=` と *`wid`* が指定されていないか、または 0 に設定されている場合、デカル転写サイズは *`hei`* から計算されます。 *`thickness`* が指定されていないか、0 に設定されている場合、ドロップシャドウはレンダリングされません。

## 例 {#section-04fdc2b60b9e4071b672bf6a913738ad}

解像度に基づいてサイズが調整され、時計回りに 20 度回転し、厚さが 2.5 インチのデカル転写の MSS で、適切なドロップ シャドウ効果が得られます。

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## 関連項目 {#section-1b116ecd60214732a1757ee1f0cf21c2}

[&#x200B; シーン座標 &#x200B;](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1)、[res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)、[attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
