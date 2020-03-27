---
description: 画像の拡大・縮小 最大解像度の画像を基準にして画像を拡大・縮小します。
seo-description: 画像の拡大・縮小 最大解像度の画像を基準にして画像を拡大・縮小します。
seo-title: scale
solution: Experience Manager
title: scale
topic: Scene7 Image Serving - Image Rendering API
uuid: db5bab94-e5c1-41fe-ab1b-5c62b6a798d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# scale{#scale}

画像の拡大・縮小 最大解像度の画像を基準にして画像を拡大・縮小します。

`scale= *`因子`*`

<table id="simpletable_AC0974B79E064BA99C1F76461BDE808A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 因子</span></span> </p> </td> 
  <td class="stentry"> <p>スケール係数（実数、&gt;0） </p></td> 
 </tr> 
</table>

## 初期設定 {#section-e9e53959b35844579f0f1d7721b71f8e}

指定しなかった場合、画像は拡大・縮小せずに使用されます。

## 例 {#section-d5526953d6434c58bb2388bd936c13b5}

[!DNL http://server/is/agm/myRootId/myImageId?scale=.5]
