---
description: SpinView.autospin
solution: Experience Manager
title: SpinView.autospin
topic: Dynamic media
uuid: 9d24ed39-e4b9-442b-bc64-c77707ff69d8
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---


# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *``*][, *``*][, *`durationdirectionspin_number`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 自動スピンアニメーションを有効または無効にします。 最適な自動スピン操作を実現するには、<span class="codeph"> maxloadradius</span>を<span class="codeph"> -1</span>に設定して、すべてのフレームをプリロードすることをお勧めします。 ただし、この結果、読み込み時間が長くなり、帯域幅使用量が増えます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 期間</span></span> </p> </td> 
   <td colname="col2"> <p> 1回のフルスピンあたりの秒数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 方向</span></span> </p> </td> 
   <td colname="col2"> <p> スピンの方向は、東向きは<span class="codeph"> 0</span>、西向きは<span class="codeph"> 1</span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> spin_number</span></span> </p> </td> 
   <td colname="col2"> <p> 自動スピンが停止する前に行われた完全な回転数。 数値は浮動小数点数です。 無限の自動スピンの場合は、<span class="codeph"> -1</span>に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-924163cb2f6542499f49894becef7fb5}

（オプション）

## 初期設定 {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## 例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
