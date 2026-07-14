---
title: ThumbnailGridView.fmt
description: ThumbnailGridView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 916ee5d1-e398-4923-9107-96f649033298
TQID: 'https://experienceleague.adobe.com/Jp3-9jcSw3-AnFXY4TXdJrXdaKNQB-F5lPAYMcDl8uI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 67
ht-degree: 4%

---

# ThumbnailGridView.fmt{#thumbnailgridview-fmt}

`[ThumbnailGridView.|<containerId>_gridView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>コンポーネントがImage Serverから画像を読み込むときに使用する画像形式を指定します。 Image Serverとクライアントブラウザーがサポートする任意の値を指定できます。 指定された形式が<span class="codeph"> -alpha</span>で終わる場合、コンポーネントは画像を透明コンテンツとしてレンダリングします。 その他のすべての画像形式では、コンポーネントは画像を不透明として扱います。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-ffe8ccc3a5f2474db47a68c2ad9a96d6}

オプション。

## 初期設定 {#section-502c098dbae1452180c7f575a1d9dc8b}

`jpeg`

## 例 {#section-5cde7b856ba646c293cfd3d79e47c507}

`fmt-png-alpha`

