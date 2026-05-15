---
title: SpinView.maxloadradius
description: SpinView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
TQID: 'https://experienceleague.adobe.com/h7jV66-f8J9UoMxsROgQrDLSN-ONyXSZ71gj75-Z7v8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">値</span></span> </p> </td> 
   <td colname="col2"> <p> SpinViewがアイドル状態の場合、各方向にプリロードするフレームの最大数を表します。 値<span class="codeph"> -1</span>を指定すると、セット内のすべてのフレームがプリロードされます。 プリロードされたフレームは、常にSpinViewが最初にロードされた元の解像度で表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> プリロードされたフレームの品質を制御します。 <span class="codeph"> 1</span> フレームに設定すると、コンポーネントのサイズに合わせて、高画質で読み込まれます。 <span class="codeph"> 0</span>に設定すると、低解像度のプレビュータイルのみが読み込まれます。 </p> <p>高解像度でのプリロードは、特に自動スピンが有効になっている場合に、エンドユーザーエクスペリエンスを向上させます。 同時に、起動時間が遅くなり、ネットワーク消費が多くなるので、注意して使用してください。 高解像度プリロードを使用する場合、プリロードされたフレームは常に、最初にコンポーネントがロードされた元の解像度になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-924163cb2f6542499f49894becef7fb5}

オプション。

## 初期設定 {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## 例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
