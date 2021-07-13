---
description: 画像を拡大・縮小します。 最大解像度の画像を基準に画像を拡大・縮小します。
solution: Experience Manager
title: scale
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 89701a15-a0b6-460d-b0c1-5e25f3305380
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 8%

---

# スケール{#scale}

画像を拡大・縮小します。 最大解像度の画像を基準に画像を拡大・縮小します。

`scale= *`因子`*`

<table id="simpletable_AC0974B79E064BA99C1F76461BDE808A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 因子</span></span> </p> </td> 
  <td class="stentry"> <p>スケール係数（実数、0より大きい） </p></td> 
 </tr> 
</table>

## 初期設定 {#section-e9e53959b35844579f0f1d7721b71f8e}

指定しなかった場合、画像は拡大・縮小されずに使用されます。

## 例 {#section-d5526953d6434c58bb2388bd936c13b5}

[!DNL http://server/is/agm/myRootId/myImageId?scale=.5]
