---
description: Swatches.enabledragging
solution: Experience Manager
title: Swatches.enabledragging
topic: Dynamic media
uuid: f676b0b1-2ce0-4409-8db6-ce162b03053b
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 6%

---


# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> マウスまたはタッチジェスチャを使用してスウォッチをスクロールする機能を有効または無効にします </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td> <p> <span class="codeph"> 0-1 </span>の範囲内の関数。 実際の速度の誤った方向に移動する場合は、<span class="codeph"> % </span>の値です。 <span class="codeph"> 1 </span>に設定すると、マウスと共に移動します。 <span class="codeph"> 0 </span>に設定した場合、正しくない方向には一切動かせません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,0.5`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enabledragging=0`
