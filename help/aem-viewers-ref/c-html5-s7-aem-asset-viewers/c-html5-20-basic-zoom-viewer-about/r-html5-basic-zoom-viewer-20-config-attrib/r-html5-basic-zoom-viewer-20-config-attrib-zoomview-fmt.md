---
title: ZoomView.fmt
description: ZoomView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 7cb75d38-a577-4e06-b679-c4e00db5059a
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 4%

---

# ZoomView.fmt{#zoomview-fmt}

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> コンポーネントが Image Server から画像を読み込むために使用する画像形式を指定します。 指定した形式が「– alpha」で終わる場合、コンポーネントは画像を透明コンテンツとしてレンダリングします。 他のすべての画像形式では、コンポーネントは画像を不透明として扱います。 コンポーネントの背景は、デフォルトで白になります。 したがって、透明にするには、背景色 CSS プロパティを「透明」に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-50bcd15223174bb79ce08b31ea03d682}

オプション。

## 初期設定 {#section-7564169749ff4a4996049ea1148cb2a5}

`jpeg`

## 例 {#section-96e69b70365f461dae4399e49044ea2f}

`fmt=png-alpha`
