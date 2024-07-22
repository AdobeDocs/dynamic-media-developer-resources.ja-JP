---
title: ZoomView.zoomstep
description: ZoomView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ded8168e-08f7-4bc0-bb8a-624bac82759e
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *`step`*[, *`limit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ステップ </span> </span> </p> </td> 
   <td colname="col2"> <p> 解像度を 2 倍に増減させるために必要なズームインおよびズームアウトアクションの回数を設定します。 各ズームアクションの解像度の変化は、1 ステップあたり 2^1 です。 <span class="codeph"> 0</span> に設定すると、1 回のズームアクションで最大解像度にズームできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> limit</span> </span> </p> </td> 
   <td colname="col2"> <p> 最大解像度を指定します。最大解像度は、フル解像度の画像を基準にします。 デフォルトは <span class="codeph"> 1.0</span> で、フル解像度を超えてズームすることはできません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-50bcd15223174bb79ce08b31ea03d682}

オプション。

## 初期設定 {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1`

## 例 {#section-96e69b70365f461dae4399e49044ea2f}

`zoomstep=2,3`
