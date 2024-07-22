---
title: SpinView.maxloadradius
description: SpinView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 値 </span></span> </p> </td> 
   <td colname="col2"> <p> SpinView がアイドル状態のときに各方向にプリロードするフレームの最大数を表します。 値が <span class="codeph">-1</span> の場合、セット内のすべてのフレームがプリロードされます。 プリロードされたフレームは、SpinView が最初にロードされた元の解像度で常に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> プリロードされたフレームの品質を制御します。 <span class="codeph">1</span> に設定すると、フレームはコンポーネントのサイズに一致する高品質でロードされます。 <span class="codeph">0 に設定すると </span> 低解像度のプレビュータイルのみが読み込まれます。 </p> <p>高解像度でプリロードすると、特に自動スピンが有効な場合に、エンドユーザーエクスペリエンスが向上します。 同時に、起動時間が遅くなり、ネットワーク消費が増加するので、注意して使用してください。 高解像度のプリロードを使用する場合、プリロードされたフレームは常に、コンポーネントが最初にロードされた元の解像度になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-924163cb2f6542499f49894becef7fb5}

オプション。

## 初期設定 {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## 例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
