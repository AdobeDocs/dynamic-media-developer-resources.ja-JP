---
title: Swatches.enabledragging
description: Swatches.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7ffdc886-5631-429f-84b4-4b32b715713d
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
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
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> 内の関数 <span class="codeph"> 0-1 </span> 範囲。 これは、 <span class="codeph"> % </span> 実際の速度の誤った方向への移動の値。 これが <span class="codeph"> 1 </span>をクリックすると、マウスと共に移動します。 これが <span class="codeph"> 0 </span>を指定した場合、正しくない方向に移動することはできません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

（オプション）

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`1,0.5`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`enabledragging=0`
