---
title: SpinView.zoomstep
description: SpinView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 919477d0-87d9-4cf7-a7c8-0fbb68c6ff96
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 3%

---

# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *`step`*[, *`limit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> ステップ </span></span> </p> </td> 
   <td colname="col2"> <p> 解像度を 2 倍に増減するために必要なズームインおよびズームアウトの回数を設定します。 各ズームアクションの解像度の変化は、1 ステップあたり 2^1 です。 <span class="codeph"> 0</span> に設定すると、1 回のズームアクションで最大解像度にズームできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 限 </span></span> </p> </td> 
   <td colname="col2"> <p> 最大解像度を指定します。最大解像度は、フル解像度の画像を基準にします。 デフォルトは <span class="codeph"> 1.0</span> で、フル解像度を超えてズームすることはできません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-924163cb2f6542499f49894becef7fb5}

オプション。

## 初期設定 {#section-7a2128fd488941948aff18421f533ccf}

`1,1`

## 例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`zoomstep=2,3`
