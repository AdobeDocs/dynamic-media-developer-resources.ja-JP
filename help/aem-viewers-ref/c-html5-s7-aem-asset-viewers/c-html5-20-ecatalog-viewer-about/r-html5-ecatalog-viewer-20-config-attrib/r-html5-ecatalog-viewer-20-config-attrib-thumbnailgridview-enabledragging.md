---
description: ThumbnailGridView.enabledragging
solution: Experience Manager
title: ThumbnailGridView.enabledragging
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: e3615e82-d8f0-427e-ab32-f7d0f2b6cbf3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 6%

---

# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

` [ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> マウスまたはタッチジェスチャを使用してスウォッチをスクロールする機能を有効または無効にします </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td> <p> <span class="codeph"> 0-1 </span>の範囲内で機能します。 実際の速度の誤った方向への移動は<span class="codeph"> % </span>の値です。 <span class="codeph"> 1 </span>に設定すると、マウスと共に移動します。 <span class="codeph"> 0 </span>に設定した場合、正しくない方向にはまったく移動できません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-831c23dea82449bfa50fd155bea365b7}

（オプション）

## 初期設定 {#section-464be2db89f34516ad93f32f7783d2b0}

`1,0.5`

## 例 {#section-e67c8807762e471bb03d6a8fb20e19d4}

`enabledragging=0`
