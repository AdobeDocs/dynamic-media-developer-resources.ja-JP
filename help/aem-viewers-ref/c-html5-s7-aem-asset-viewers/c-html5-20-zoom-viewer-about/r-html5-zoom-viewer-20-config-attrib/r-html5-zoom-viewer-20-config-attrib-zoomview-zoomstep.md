---
title: ZoomView.zoomstep
description: ZoomView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: bcd153f3-7a87-4e8f-825b-fc4a136de1dc
TQID: 'https://experienceleague.adobe.com/7wu--abb-d3xqm2uJzgyubkb7SmaDVStd0-oCNEXYqc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 3%

---

# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *` ステップ `*[, *`制限`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> ステップ </span></span> </p> </td> 
   <td colname="col2"> <p> 解像度を2倍に増減するために必要なズームインとズームアウトのアクションの数を設定します。 各ズームアクションの解像度の変更は、ステップごとに2^1です。 1回のズームアクションで完全な解像度にズームするには、<span class="codeph"> 0</span>に設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">制限</span></span> </p> </td> 
   <td colname="col2"> <p> フル解像度イメージに対する最大ズーム解像度を指定します。 デフォルトは<span class="codeph"> 1.0</span>で、完全な解像度を超えるズームは許可されていません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`1,1`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`zoomstep=2,3`
