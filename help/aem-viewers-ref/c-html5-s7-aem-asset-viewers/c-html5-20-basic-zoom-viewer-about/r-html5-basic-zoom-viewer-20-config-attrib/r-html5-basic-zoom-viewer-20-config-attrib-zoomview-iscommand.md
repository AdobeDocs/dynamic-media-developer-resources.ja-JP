---
description: ZoomView.iscommand
solution: Experience Manager
title: ZoomView.iscommand
feature: Dynamic Media Classic，ビューア，SDK/API，ズーム
role: Developer,User
exl-id: d1f54ef2-4ed4-4fb6-9913-98bf194f9afc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 7%

---

# ZoomView.iscommand{#zoomview-iscommand}

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> iscommand</span> </span> </p> </td> 
   <td colname="col2"> <p> ズーム画像に適用される画像サービングコマンド文字列。 URLで指定する場合、 <span class="codeph"> &amp;</span>と<span class="codeph"> =</span>はすべて、 <span class="codeph"> %26</span>と<span class="codeph"> %3D</span>にそれぞれHTTPエンコードする必要があります。 </p> <p> <p>注意： 画像のサイズ変更操作コマンドはサポートされていません。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-50bcd15223174bb79ce08b31ea03d682}

（オプション）

## 初期設定 {#section-7564169749ff4a4996049ea1148cb2a5}

なし

## 例 {#section-96e69b70365f461dae4399e49044ea2f}

ビューアのURLで指定する場合：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

configデータで指定する場合：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
