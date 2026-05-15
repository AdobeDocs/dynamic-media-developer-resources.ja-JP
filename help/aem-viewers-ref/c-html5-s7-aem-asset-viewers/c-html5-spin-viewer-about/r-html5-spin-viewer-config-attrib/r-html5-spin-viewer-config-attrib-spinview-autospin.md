---
title: SpinView.autospin
description: SpinView.autospin
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 16276e07-5494-4fd9-bd77-e77a46c57fd1
TQID: 'https://experienceleague.adobe.com/ZQj4mwz-MZWHf8MeY-hrrESZLucBeqXpGQV6tnD-U9w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 5%

---

# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *`期間`*][, *`方向`*][, *` スピン数`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> 自動スピンアニメーションを有効または無効にします。 最適な自動スピンエクスペリエンスを実現するには、<span class="codeph"> maxloadradius</span>を<span class="codeph"> -1</span>に設定して、すべてのフレームをプリロードすることをお勧めします。 ただし、この設定では、読み込み時間が長くなり、帯域幅の使用率が高くなることに注意してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">期間</span></span> </p> </td> 
   <td colname="col2"> <p> フルスピン 1回あたりの秒数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">方向</span></span> </p> </td> 
   <td colname="col2"> <p> 東を回転する<span class="codeph"> 0</span>と西を回転する<span class="codeph"> 1</span>のスピン方向。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> spin_number</span></span> </p> </td> 
   <td colname="col2"> <p> オートスピンが停止する前に行われた完全な回転の数。 数値は浮動小数点数です。 無限自動スピンの場合は<span class="codeph"> -1</span>に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-924163cb2f6542499f49894becef7fb5}

オプション。

## 初期設定 {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## 例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
