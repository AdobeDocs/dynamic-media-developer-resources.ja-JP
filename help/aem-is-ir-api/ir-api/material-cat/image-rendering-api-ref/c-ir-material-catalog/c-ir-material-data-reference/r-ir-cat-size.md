---
description: デカールのサイズ。 デカールマテリアルオブジェクトの幅、高さ、厚さ。
solution: Experience Manager
title: サイズ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 5%

---

# サイズ{#size}

デカールのサイズ。 デカールマテリアルオブジェクトの幅、高さ、厚さ。

## プロパティ {#section-967bf1112eec4032a91ed0c8a7b10a07}

コンマで区切られた 3 つの実数。 負の値にすることはできません。 未使用の値を 0 に設定します。 末尾のゼロは省略できます。

幅と高さの両方を指定するのは、画像が指定のサイズに合わせて拡大される場合のみです（縦横比が変わる場合があります）。 幅または高さを設定して、画像を縦横比を保って拡大/縮小します。 幅と高さの両方を 0 に設定して、 `catalog::Resolution`をクリックして、オブジェクトのサイズを指定します。

デカールオブジェクトにドロップシャドウを追加するには、厚さの値を指定します。 デカール材料の場合はオプションで、他のすべての材料では無視されます。

## 初期設定 {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. これは、デカールのサイズが catalog::Resolution に基づいて決定され、オブジェクトの厚さがない（したがって、ドロップシャドウがレンダリングされない）ことを示します。

## 例 {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>デカールは 12 x 3 インチのサイズに強制され、厚さはありません（ドロップシャドウはありません）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>デカールの幅は 5 インチで、高さは画像の縦横比で決まり、ドロップシャドウは 1 インチの厚さに基づいてレンダリングされます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>デカールの幅と高さは、catalog::Resolution によって決まり、厚さは 1/2 インチです。 </p></td> 
 </tr> 
</table>

## 関連項目 {#section-31a164e781d14e92bd9d379d3c329e92}

[catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
