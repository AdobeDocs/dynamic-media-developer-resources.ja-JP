---
title: PageView.zoomstep
description: PageView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 64cce312-c13b-49c7-af85-3349ff5c4322
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# PageView.zoomstep{#pageview-zoomstep}

` [PageView.|<containerId>_pageView.]zoomstep= *`step`*[, *`limit`*]`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> ステップ </span></span> </p> </td> 
   <td colname="col2"> <p> 解像度を 2 倍に増減させるために必要なズームインおよびズームアウトアクションの回数を設定します。 各ズームアクションの解像度の変化は、1 ステップあたり 2^1 です。 <span class="codeph"> 0</span> に設定すると、1 回のズームアクションで最大解像度にズームできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 限 </span></span> </p> </td> 
   <td colname="col2"> <p> 最大解像度を指定します。最大解像度は、フル解像度の画像を基準にします。 デフォルトは <span class="codeph"> 1.0</span> で、フル解像度を超えてズームすることはできません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-636d35a4791447039f1902973f568320}

オプション。

## 初期設定 {#section-ad8a5fe2383e4c228bf177a41b53d921}

`1,1`

## 例 {#section-1e20672d42c845bd84f02f88cbc53efc}

`zoomstep=2,3`
