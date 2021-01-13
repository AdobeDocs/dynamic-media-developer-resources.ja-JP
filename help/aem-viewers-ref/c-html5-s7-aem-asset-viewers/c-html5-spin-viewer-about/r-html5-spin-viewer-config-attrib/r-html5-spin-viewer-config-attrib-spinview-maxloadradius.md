---
description: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
topic: Dynamic media
uuid: 8f475fa8-92d1-4663-bc12-1e65b76076ba
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---


# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> 各方向でSpinViewがアイドルの場合にプリロードするフレームの最大数を表します。 値<span class="codeph"> -1</span>は、セット内のすべてのフレームをプリロードします。 プリロードされたフレームは、常にSpinViewが最初に読み込まれた元の解像度で表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> プリロードされたフレームの品質を制御します。 <span class="codeph"> 1</span>フレームを高品質でロードする場合は、コンポーネントのサイズに合わせます。 <span class="codeph"> 0</span>に設定した場合は、低解像度のプレビュータイルのみが読み込まれます。 </p> <p>高解像度でプリロードすると、特に自動スピンが有効な場合に、エンドユーザーの操作性が向上します。 同時に、開始時間が遅くなり、ネットワーク消費が増えるので、注意して使用してください。 高解像度のプリロードを使用する場合、プリロードされたフレームは常に、コンポーネントが最初に読み込まれた元の解像度になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-924163cb2f6542499f49894becef7fb5}

（オプション）

## 初期設定 {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## 例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
