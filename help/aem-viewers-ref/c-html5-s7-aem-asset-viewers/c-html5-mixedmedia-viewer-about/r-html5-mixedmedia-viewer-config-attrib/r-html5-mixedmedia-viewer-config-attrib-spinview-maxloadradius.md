---
title: SpinView.maxloadradius
description: SpinViewがアイドル状態の場合、各方向にプリロードするフレームの最大数を表します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
TQID: 'https://experienceleague.adobe.com/SqjidvUT9DCONC8u-rtlhUem-5M5bu0ye4sZPhiHcds'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 158
ht-degree: 1%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

SpinViewがアイドル状態の場合、各方向にプリロードするフレームの最大数を表します。

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">値</span></span> </p> </td> 
   <td colname="col2"> <p> 値<span class="codeph"> -1</span>を指定すると、セット内のすべてのフレームがプリロードされます。 プリロードされたフレームは、常にSpinViewが最初にロードされた元の解像度で表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> プリロードされたフレームの品質を制御します。 </p> <p><span class="codeph"> 1</span>に設定すると、フレームはコンポーネントのサイズに合わせて高画質で読み込まれます。 </p> <p><span class="codeph"> 0</span>に設定すると、低解像度のプレビュータイルのみが読み込まれます。</p> <p>高解像度でのプリロードは、特に自動スピンが有効になっている場合に、ユーザーエクスペリエンスを向上させます。 同時に、開始時間が遅くなり、ネットワーク消費量が多くなるため、慎重に使用する必要があります。 高解像度プリロードを使用する場合、プリロードされたフレームは常に、コンポーネントが最初にロードされた元の解像度になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
