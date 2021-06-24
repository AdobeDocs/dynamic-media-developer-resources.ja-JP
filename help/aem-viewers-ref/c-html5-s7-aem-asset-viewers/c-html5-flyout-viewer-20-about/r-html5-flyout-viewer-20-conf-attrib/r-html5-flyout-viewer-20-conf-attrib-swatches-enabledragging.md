---
description: Swatches.enabledragging
solution: Experience Manager
title: Swatches.enabledragging
feature: Dynamic Media Classic，ビューア，SDK/API，フライアウト
role: Developer,Business Practitioner
exl-id: 7ffdc886-5631-429f-84b4-4b32b715713d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '82'
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
   <td> <p> <span class="codeph"> 0-1 </span>の範囲内で機能します。 実際の速度の誤った方向への移動は<span class="codeph"> % </span>の値です。 <span class="codeph"> 1 </span>に設定すると、マウスと共に移動します。 <span class="codeph"> 0 </span>に設定した場合、正しくない方向にはまったく移動できません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

（オプション）

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`1,0.5`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`enabledragging=0`
