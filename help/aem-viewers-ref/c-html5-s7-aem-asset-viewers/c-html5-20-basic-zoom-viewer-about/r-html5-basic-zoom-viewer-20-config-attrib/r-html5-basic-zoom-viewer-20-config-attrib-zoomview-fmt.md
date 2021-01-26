---
description: ZoomView.fmt
solution: Experience Manager
title: ZoomView.fmt
topic: Dynamic Media
uuid: b118e441-f128-4dfd-a82e-62ec4d1ebf84
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 5%

---


# ZoomView.fmt{#zoomview-fmt}

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> コンポーネントでImage Serverからの画像の読み込みに使用する画像形式を指定します。 末尾が「 —alpha」の形式を指定すると、画像が透明のコンテンツとしてレンダリングされます。 その他のすべての画像形式の場合、画像は不透明として扱われます。 コンポーネントの背景はデフォルトで白になります。 したがって、透明にするには、CSSプロパティbackground-colorをtransparentに指定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-50bcd15223174bb79ce08b31ea03d682}

（オプション）

## 初期設定 {#section-7564169749ff4a4996049ea1148cb2a5}

`jpeg`

## 例 {#section-96e69b70365f461dae4399e49044ea2f}

`fmt=png-alpha`
