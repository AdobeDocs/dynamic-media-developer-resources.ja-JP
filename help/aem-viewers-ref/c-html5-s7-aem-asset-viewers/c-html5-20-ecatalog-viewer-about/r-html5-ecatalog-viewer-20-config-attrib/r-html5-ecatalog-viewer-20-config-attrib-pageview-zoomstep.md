---
title: PageView.zoomstep
description: PageView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 64cce312-c13b-49c7-af85-3349ff5c4322
TQID: 'https://experienceleague.adobe.com/cEDD4fmF-pm2VHOOAbkZlGiJ6MTisLVdKYxwDoighvA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 82
ht-degree: 3%

---

# PageView.zoomstep{#pageview-zoomstep}

` [PageView.|<containerId>_pageView.]zoomstep= *` ステップ `*[, *`制限`*]`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> ステップ </span></span> </p> </td> 
   <td colname="col2"> <p> 解像度を2倍増減するために必要なズームインとズームアウトのアクションの数を設定します。 各ズームアクションの解像度の変更は、ステップごとに2^1です。 1回のズームアクションで完全な解像度にズームするには、<span class="codeph"> 0</span>に設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">制限</span></span> </p> </td> 
   <td colname="col2"> <p> フル解像度イメージに対する最大ズーム解像度を指定します。 デフォルトは<span class="codeph"> 1.0</span>で、完全な解像度を超えるズームは許可されていません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-636d35a4791447039f1902973f568320}

オプション。

## 初期設定 {#section-ad8a5fe2383e4c228bf177a41b53d921}

`1,1`

## 例 {#section-1e20672d42c845bd84f02f88cbc53efc}

`zoomstep=2,3`
