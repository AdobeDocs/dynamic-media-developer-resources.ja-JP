---
description: デカールのサイズ デカールマテリアルオブジェクトの幅、高さ、厚さ。
seo-description: デカールのサイズ デカールマテリアルオブジェクトの幅、高さ、厚さ。
seo-title: サイズ
solution: Experience Manager
title: サイズ
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 07d41f71-e18d-4559-afc7-75dc1c45be93
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 5%

---


# サイズ{#size}

デカールのサイズ デカールマテリアルオブジェクトの幅、高さ、厚さ。

## プロパティ {#section-967bf1112eec4032a91ed0c8a7b10a07}

カンマで区切られた3つの実数です。 負の値は指定できません。 未使用の値を0に設定します。 末尾のゼロは省略できます。

幅と高さは、画像を指定したサイズに合わせて拡大する場合にのみ指定します（縦横比が変わる場合があります）。 幅または高さを設定して、画像を縦横比を維持したまま拡大・縮小します。 幅と高さの両方を0に設定して、`catalog::Resolution`を使用してオブジェクトのサイズを決定します。

厚さの値を指定して、デカールオブジェクトにドロップシャドウを追加します。 デカル転写材のオプションです。他のすべての材料では無視されます。

## 初期設定 {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. これは、デカル転写のサイズがcatalog::Resolutionに基づいて決定され、オブジェクトの厚さがないことを示します（ドロップシャドウはレンダリングされません）。

## 例 {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>デカールのサイズは12 x 3インチに強制され、厚さはありません（ドロップシャドウはありません）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>デカールの幅は5インチで、高さはイメージの縦横比で決まり、ドロップシャドウは1インチの厚さに基づいてレンダリングされます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>デカル転写の幅と高さはcatalog::Resolutionで決まり、厚さは1/2インチです。 </p></td> 
 </tr> 
</table>

## 関連項目 {#section-31a164e781d14e92bd9d379d3c329e92}

[catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
