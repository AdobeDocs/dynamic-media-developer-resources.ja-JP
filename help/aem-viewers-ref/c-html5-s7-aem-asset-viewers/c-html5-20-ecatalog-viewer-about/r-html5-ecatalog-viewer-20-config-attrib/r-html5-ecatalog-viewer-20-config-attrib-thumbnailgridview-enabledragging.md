---
title: ThumbnailGridView.enabledragging
description: ThumbnailGridView.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e3615e82-d8f0-427e-ab32-f7d0f2b6cbf3
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

` [ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td> <p> マウスまたはタッチ ジェスチャを使用してスウォッチをスクロールする機能を有効または無効にします </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> <span class="codeph"> 0 ～ 1 </span> の範囲内の関数。 実際の速度の誤った方向に移動する場合の <span class="codeph"> %</span> 値です。 1</span> に設定 <span class="codeph"> ると、マウスと一緒に移動します。 0</span> に設定 <span class="codeph"> ると、まったく間違った方向に移動することはできません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-831c23dea82449bfa50fd155bea365b7}

オプション。

## 初期設定 {#section-464be2db89f34516ad93f32f7783d2b0}

`1,0.5`

## 例 {#section-e67c8807762e471bb03d6a8fb20e19d4}

`enabledragging=0`
