---
title: SpinView.maxloadradius
description: SpinView がアイドル状態の場合に各方向にプリロードするフレームの最大数を表します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

SpinView がアイドル状態の場合に各方向にプリロードするフレームの最大数を表します。

` [SpinView.|<containerId>_spinView.]maxloadradius= *`値`*[, *`highRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 値</span></span> </p> </td> 
   <td colname="col2"> <p> 値： <span class="codeph"> -1</span> セット内のすべてのフレームをプリロードします。 プリロードされたフレームは、常に、SpinView が最初に読み込まれた元の解像度で表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> プリロードされたフレームの品質を制御します。 </p> <p>に設定する場合 <span class="codeph"> 1</span> フレームは、コンポーネントのサイズに合わせて高品質で読み込まれます。 </p> <p>に設定する場合 <span class="codeph"> 0</span> 低解像度のプレビュータイルのみが読み込まれます。</p> <p>高解像度でプリロードすると、特に自動スピンが有効な場合に、ユーザーのエクスペリエンスが向上します。 同時に、開始時間が長くなり、ネットワーク消費が増加するので、慎重に使用する必要があります。 高解像度のプリロードを使用する場合、プリロードされたフレームは常に、コンポーネントが最初に読み込まれた元の解像度になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
