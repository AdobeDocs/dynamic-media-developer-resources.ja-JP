---
description: 画像の拡大・縮小 最大解像度の画像を基準にして画像を拡大・縮小します。
solution: Experience Manager
title: scale
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 8%

---


# scale{#scale}

画像の拡大・縮小 最大解像度の画像を基準にして画像を拡大・縮小します。

`scale= *`因子`*`

<table id="simpletable_AC0974B79E064BA99C1F76461BDE808A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 因子</span></span> </p> </td> 
  <td class="stentry"> <p>尺度係数（実数、&gt;0） </p></td> 
 </tr> 
</table>

## 初期設定 {#section-e9e53959b35844579f0f1d7721b71f8e}

指定しなかった場合、画像は拡大・縮小されずに使用されます。

## 例 {#section-d5526953d6434c58bb2388bd936c13b5}

[!DNL http://server/is/agm/myRootId/myImageId?scale=.5]
