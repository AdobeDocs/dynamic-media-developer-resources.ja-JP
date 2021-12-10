---
title: Swatches.fmt
description: Swatches.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 8b47839a-ef3b-45ae-8e8d-5c9391d71d44
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 5%

---

# Swatches.fmt{#swatches-fmt}

`[Swatches.|<containerId>_swatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>コンポーネントが Image Server からの画像の読み込みに使用する画像形式を指定します。 指定した形式が <span class="codeph"> -alpha</span>を指定しない場合、コンポーネントは画像を透明なコンテンツとしてレンダリングします。 その他のすべての画像形式では、画像は不透明として扱われます。 コンポーネントの背景は、デフォルトで白です。 したがって、背景を透明にするには、 <span class="codeph"> background-color</span> CSS プロパティをに設定 <span class="codeph"> 透明</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt-png-alpha`
