---
title: ZoomView.zoomstep
description: ZoomView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ded8168e-08f7-4bc0-bb8a-624bac82759e
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---

# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *`手順`*[, *`制限`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 手順</span> </span> </p> </td> 
   <td colname="col2"> <p> 解像度を 1/2 に増減するために必要なズームインおよびズームアウト操作の回数を設定します。 各ズーム操作の解像度の変更は、1 ステップあたり 2^1 です。 に設定 <span class="codeph"> 0</span> 1 回のズーム操作で最大解像度までズームする場合。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 制限</span> </span> </p> </td> 
   <td colname="col2"> <p> 最大解像度の画像を基準とする最大ズーム解像度を指定します。 デフォルトはです。 <span class="codeph"> 1.0</span>：最大解像度以上にズームできません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-50bcd15223174bb79ce08b31ea03d682}

（オプション）

## 初期設定 {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1`

## 例 {#section-96e69b70365f461dae4399e49044ea2f}

`zoomstep=2,3`
