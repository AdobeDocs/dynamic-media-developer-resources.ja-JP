---
title: サイズ
description: デカールのサイズ： デカール マテリアル オブジェクトの幅、高さ、厚さ。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
TQID: 'https://experienceleague.adobe.com/HLyEmmOch9kiHQ3sqpvHCQiHOBltjQcsZaDu0na1-Ww'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 217
ht-degree: 5%

---

# サイズ{#size}

デカールのサイズ： デカール マテリアル オブジェクトの幅、高さ、厚さ。

## プロパティ {#section-967bf1112eec4032a91ed0c8a7b10a07}

コンマで区切られた3つの実数。 否定的であってはなりません。 未使用の値を0に設定します。 末尾のゼロは省略できます。

指定したサイズに合わせて画像を引き伸ばす必要がある場合にのみ、幅と高さの両方を指定します（縦横比が変更される場合があります）。 幅または高さを設定して、画像を比例して拡大・縮小します。 幅と高さの両方を0に設定して、`catalog::Resolution`を使用してオブジェクトサイズを決定します。

デカールオブジェクトにドロップシャドウを追加する太さの値を指定します。 デカール マテリアルの場合はオプションで、他のすべてのマテリアルでは無視されます。

## 初期設定 {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. これは、デカールのサイズがcatalog::Resolutionに基づいて決定され、オブジェクトに厚みがないことを示します（したがって、ドロップシャドウはレンダリングされません）。

## 例 {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>デカールのサイズは12 x 3 インチに強制され、厚みはありません（ドロップシャドウはありません）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>デカールの幅は5 インチで、高さは画像の縦横比によって決まり、ドロップシャドウは1 インチの厚さに基づいてレンダリングされます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>デカールの幅と高さはcatalog::Resolutionによって決まり、厚さは1/2 インチです。 </p></td> 
 </tr> 
</table>

## 関連項目 {#section-31a164e781d14e92bd9d379d3c329e92}

[catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)

