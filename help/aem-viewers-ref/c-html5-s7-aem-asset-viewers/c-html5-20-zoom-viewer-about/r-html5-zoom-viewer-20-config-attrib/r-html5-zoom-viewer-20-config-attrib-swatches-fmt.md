---
title: Swatches.fmt
description: Swatches.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 8b47839a-ef3b-45ae-8e8d-5c9391d71d44
TQID: 'https://experienceleague.adobe.com/-G0MTKCw40OwMk5pkB6fcLzMu81eql24AnnDHZthQ6U'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 3%

---

# Swatches.fmt{#swatches-fmt}

`[Swatches.|<containerId>_swatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>コンポーネントがImage Serverから画像を読み込むときに使用する画像形式を指定します。 指定された形式が<span class="codeph"> -alpha</span>で終わる場合、コンポーネントは画像を透明コンテンツとしてレンダリングします。 その他のすべての画像形式では、コンポーネントは画像を不透明として扱います。 デフォルトでは、コンポーネントの背景は白です。 したがって、背景を透明にするには、<span class="codeph"> background-color</span> CSS プロパティを<span class="codeph"> transparent</span>に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt-png-alpha`

