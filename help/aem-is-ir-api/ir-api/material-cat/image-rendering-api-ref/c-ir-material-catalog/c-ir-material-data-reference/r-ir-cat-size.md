---
title: サイズ
description: デカル転写サイズ。 デカール マテリアル オブジェクトの幅、高さ、厚さ
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 3%

---

# サイズ{#size}

デカル転写サイズ。 デカール マテリアル オブジェクトの幅、高さ、厚さ

## プロパティ {#section-967bf1112eec4032a91ed0c8a7b10a07}

コンマで区切られた 3 つの実数。 負の値は指定できません。 未使用の値を 0 に設定します。 末尾のゼロは省略できます。

指定したサイズに合わせて画像を引き伸ばす必要がある場合にのみ、幅と高さの両方を指定します（アスペクト比が変更される可能性があります）。 幅または高さを設定して、画像を均等に拡大縮小します。 幅と高さの両方を 0 に設定すると、`catalog::Resolution` を使用してオブジェクトのサイズを決定できます。

デカル転写オブジェクトにドロップ シャドウを追加するには、厚さの値を指定します。 デカル転写マテリアルではオプションで、他のすべてのマテリアルでは無視されます。

## 初期設定 {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0。 これは、デカル転写のサイズが catalog::Resolution に基づいて決定され、オブジェクトに厚みがないことを示します（したがって、ドロップ シャドウはレンダリングされません）。

## 例 {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>デカル転写のサイズは 12 x 3 インチに制限され、厚さはありません（つまり、影は付きません）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>デカールの幅は 5 インチで、高さはイメージのアスペクト比によって決まり、ドロップシャドウは 1 インチの厚さに基づいてレンダリングされます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>デカールの幅と高さは catalog::Resolution によって決定され、1/2 インチの厚さになります。 </p></td> 
 </tr> 
</table>

## 関連項目 {#section-31a164e781d14e92bd9d379d3c329e92}

[カタログ：：解像度](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
