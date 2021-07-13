---
description: デカルのサイズ デカールマテリアルオブジェクトの幅、高さ、厚さ。
solution: Experience Manager
title: サイズ
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 5%

---

# サイズ{#size}

デカルのサイズ デカールマテリアルオブジェクトの幅、高さ、厚さ。

## プロパティ {#section-967bf1112eec4032a91ed0c8a7b10a07}

コンマで区切った3つの実数。 負の値にすることはできません。 未使用の値を0に設定します。 末尾のゼロは省略できます。

指定したサイズに合わせて画像を拡大する場合にのみ、幅と高さの両方を指定します（縦横比が変わる場合があります）。 幅または高さを設定して、画像を比例して拡大/縮小します。 幅と高さの両方を0に設定し、`catalog::Resolution`を使用してオブジェクトのサイズを決定します。

デカールオブジェクトにドロップシャドウを追加するには、厚さの値を指定します。 デカール材料の場合はオプションで、他の材料では無視されます。

## 初期設定 {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. これは、デカル転写のサイズがcatalog::Resolutionに基づいて決定され、オブジェクトの厚さがないことを示します（したがって、ドロップシャドウはレンダリングされません）。

## 例 {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>デカールは12 x 3インチのサイズに強制され、厚さはありません（ドロップシャドウなし）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>デカールの幅は5インチで、高さは画像の縦横比で決まり、ドロップシャドウは1インチの厚さに基づいてレンダリングされます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>デカールの幅と高さは、catalog::Resolutionによって決まり、厚さは1/2インチです。 </p></td> 
 </tr> 
</table>

## 関連項目 {#section-31a164e781d14e92bd9d379d3c329e92}

[catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
