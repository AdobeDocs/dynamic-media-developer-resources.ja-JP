---
title: SpinView.zoomstep
description: SpinView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 919477d0-87d9-4cf7-a7c8-0fbb68c6ff96
TQID: 'https://experienceleague.adobe.com/7EPprL4pjlCHtiIfz2-6pmWvwfV3DZINE4wjjkkRXNM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 3%

---

# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *` ステップ `*[, *`制限`*]`

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

## プロパティ {#section-924163cb2f6542499f49894becef7fb5}

オプション。

## 初期設定 {#section-7a2128fd488941948aff18421f533ccf}

`1,1`

## 例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`zoomstep=2,3`
