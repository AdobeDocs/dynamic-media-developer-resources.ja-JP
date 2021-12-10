---
title: ZoomView.zoomstep
description: ZoomView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: bcd153f3-7a87-4e8f-825b-fc4a136de1dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 7%

---

# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *`手順`*[, *`制限`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 手順</span></span> </p> </td> 
   <td colname="col2"> <p> 解像度を 2 倍に増減するために必要なズームインおよびズームアウト操作の数を設定します。 各ズーム操作の解像度の変更は、1 ステップあたり 2^1 です。 に設定 <span class="codeph"> 0</span> 1 回のズーム操作で最大解像度までズームする場合。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 制限</span></span> </p> </td> 
   <td colname="col2"> <p> 最大解像度の画像を基準とする最大ズーム解像度を指定します。 デフォルトはです。 <span class="codeph"> 1.0</span>：最大解像度以上にズームできません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`1,1`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`zoomstep=2,3`
