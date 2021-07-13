---
description: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
feature: Dynamic Media Classic，ビューア，SDK/API，スピンセット
role: Developer,User
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> SpinViewがアイドル状態の場合に、各方向にプリロードする最大フレーム数を表します。 値<span class="codeph"> -1</span>は、セット内のすべてのフレームをプリロードします。 プリロードされたフレームは、常に、SpinViewが最初に読み込まれた元の解像度で表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> プリロードされたフレームの品質を制御します。 <span class="codeph"> 1</span>フレームを高品質でロードする場合は、コンポーネントのサイズに合わせます。 <span class="codeph"> 0</span>に設定すると、低解像度のプレビュータイルのみが読み込まれます。 </p> <p>高解像度でプリロードすると、特に自動スピンが有効な場合に、エンドユーザーの操作性が向上します。 同時に、開始時間が遅くなり、ネットワーク消費が増えるので、注意して使用してください。 高解像度のプリロードを使用する場合、プリロードされたフレームは常に、コンポーネントが最初に読み込まれた元の解像度になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-924163cb2f6542499f49894becef7fb5}

（オプション）

## 初期設定 {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## 例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
