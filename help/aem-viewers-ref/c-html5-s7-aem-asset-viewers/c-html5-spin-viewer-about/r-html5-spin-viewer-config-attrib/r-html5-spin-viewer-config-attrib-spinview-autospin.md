---
title: SpinView.autospin
description: SpinView.autospin
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 16276e07-5494-4fd9-bd77-e77a46c57fd1
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 2%

---

# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *`duration`*][, *`direction`*][, *`spin_number`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> 自動スピンアニメーションを有効または無効にします。 最適な自動スピンを実現するには、すべてのフレームをプリロードすることをお勧めします。それには <span class="codeph"> maxloadradius</span> を <span class="codeph">-1</span> に設定します。 ただし、この設定を使用すると、読み込み時間が長くなり、帯域幅の使用量が増えることに注意してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duration</span></span> </p> </td> 
   <td colname="col2"> <p> 1 回のフルスピンあたりの秒数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 方向 </span></span> </p> </td> 
   <td colname="col2"> <p> スピン方向は、東にスピンする場合は <span class="codeph"> 0</span>、西にスピンする場合は <span class="codeph"> 1</span> です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> spin_number</span></span> </p> </td> 
   <td colname="col2"> <p> オートスピンが停止する前に行われた完全な回転の回数です。 数値は浮動小数点数です。 無限オートスピンの場合は <span class="codeph">-1</span> に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-924163cb2f6542499f49894becef7fb5}

オプション。

## 初期設定 {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## 例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
