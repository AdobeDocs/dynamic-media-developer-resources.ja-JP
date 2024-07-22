---
title: SpinView.maxloadradius
description: SpinView がアイドル状態のときに各方向にプリロードするフレームの最大数を表します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

SpinView がアイドル状態のときに各方向にプリロードするフレームの最大数を表します。

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 値 </span></span> </p> </td> 
   <td colname="col2"> <p> 値が <span class="codeph">-1</span> の場合、セット内のすべてのフレームがプリロードされます。 プリロードされたフレームは、SpinView が最初にロードされた元の解像度で常に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> プリロードされたフレームの品質を制御します。 </p> <p><span class="codeph">1 に設定すると </span> フレームはコンポーネントのサイズに一致する高品質で読み込まれます。 </p> <p><span class="codeph">0 に設定すると </span> 低解像度のプレビュータイルのみが読み込まれます。</p> <p>高解像度でプリロードすると、特に自動スピンが有効な場合に、ユーザーエクスペリエンスが向上します。 同時に、起動時間が遅くなり、ネットワーク消費が増加するので、注意して使用する必要があります。 高解像度プリロードを使用した場合、プリロードされたフレームは常に、コンポーネントが最初にロードされた元の解像度になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
