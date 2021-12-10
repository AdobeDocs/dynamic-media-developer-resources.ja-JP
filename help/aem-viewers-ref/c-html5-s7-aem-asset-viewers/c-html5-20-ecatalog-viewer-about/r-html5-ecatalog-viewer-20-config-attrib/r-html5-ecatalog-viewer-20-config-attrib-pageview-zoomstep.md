---
title: PageView.zoomstep
description: PageView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 64cce312-c13b-49c7-af85-3349ff5c4322
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# PageView.zoomstep{#pageview-zoomstep}

` [PageView.|<containerId>_pageView.]zoomstep= *`手順`*[, *`制限`*]`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 手順</span></span> </p> </td> 
   <td colname="col2"> <p> 解像度を 1/2 に増減するために必要なズームインおよびズームアウト操作の回数を設定します。 各ズーム操作の解像度の変更は、1 ステップあたり 2^1 です。 に設定 <span class="codeph"> 0</span> 1 回のズーム操作で最大解像度までズームする場合。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 制限</span></span> </p> </td> 
   <td colname="col2"> <p> 最大解像度の画像を基準とする最大ズーム解像度を指定します。 デフォルトはです。 <span class="codeph"> 1.0</span>：最大解像度以上にズームできません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-636d35a4791447039f1902973f568320}

（オプション）

## 初期設定 {#section-ad8a5fe2383e4c228bf177a41b53d921}

`1,1`

## 例 {#section-1e20672d42c845bd84f02f88cbc53efc}

`zoomstep=2,3`
