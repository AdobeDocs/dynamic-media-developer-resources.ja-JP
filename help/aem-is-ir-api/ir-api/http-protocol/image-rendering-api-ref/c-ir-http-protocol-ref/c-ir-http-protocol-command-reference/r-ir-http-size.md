---
title: サイズ
description: デカールのサイズ： デカール マテリアルのサイズを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 756d8b9f-076a-48d6-95c9-e0d6caeed3dd
TQID: 'https://experienceleague.adobe.com/Dlc-HhO8gjpNds-8-cv3vCxILlTePVblpu1D1MP8eN0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 220
ht-degree: 2%

---

# サイズ{#size}

デカールのサイズ： デカール マテリアルのサイズを指定します。

` size= *`width,height`*[ *`,thickness`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> 幅<span class="varname">、高さ</span> </p> </td> 
  <td class="stentry"> <p>シーンの座標単位（通常はインチ）（実数、実数）でのデカール オブジェクトのサイズ。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">の厚さ</span> </p> </td> 
  <td class="stentry"> <p>シーンの座標単位（通常はインチ）におけるデカール オブジェクトの太さ（実数）。 </p> </td> 
 </tr> 
</table>

幅も高さも0でない場合、画像は指定された正確なサイズに拡大/縮小され、画像の縦横比は保持されません。 いずれかの値を0に設定すると、画像の縦横比が保持されます。

*`thickness`*&#x200B;が指定されている場合、周辺光量補正オブジェクトが適切な光ベクトルを定義すると、ドロップシャドウがレンダリングされます。 ドロップシャドウ レンダリングを無効にするには、*`thickness`*&#x200B;を0に設定します。

## プロパティ {#section-818e01e91fed4015951189c818ef28d8}

マテリアル属性： デカールでのみ使用されます。他のすべてのマテリアルでは無視されます。 幅または高さが0より大きい場合、`res=`は無視されます。 値は負の値にすることはできません。

## 初期設定 {#section-f91f516c6af54f0eb4d8c964b923cae0}

デカール素材がカタログ エントリに基づいている場合は`catalog::Size`。そうでない場合は`size=0,0,0`。 *`wid`*&#x200B;と&#x200B;*`hei`*&#x200B;が指定されていないか、0に設定されている場合、デカール サイズは`res=`から計算されます。 *`thickness`*&#x200B;が指定されていないか0に設定されている場合、ドロップシャドウはレンダリングされません。

## 例 {#section-04fdc2b60b9e4071b672bf6a913738ad}

解像度に基づいてサイズを調整し、時計回りに20°回転し、適切なドロップシャドウ効果を得るために、2.5 インチの厚みを持つデカールのMSS。

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## 関連項目 {#section-1b116ecd60214732a1757ee1f0cf21c2}

[&#x200B; シーン座標](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1)、[res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)、[属性：：解像度](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)

