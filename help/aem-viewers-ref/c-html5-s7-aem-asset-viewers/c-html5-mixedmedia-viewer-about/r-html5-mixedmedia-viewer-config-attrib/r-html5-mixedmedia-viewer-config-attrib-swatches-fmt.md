---
title: Swatches.fmt
description: Swatches.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 043196c8-63ab-439e-a28f-b76d1467f26e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 4%

---

# Swatches.fmt{#swatches-fmt}

`[Swatches.|<containerId>_swatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>コンポーネントが Image Server から画像を読み込むために使用する画像形式を指定します。 指定した形式が – alpha</span> で終わ <span class="codeph"> 場合、コンポーネントは画像を透明コンテンツとしてレンダリングします。 他のすべての画像形式では、コンポーネントは画像を不透明として扱います。 コンポーネントの背景は、デフォルトで白になります。 したがって、背景を透明にするには、<span class="codeph"> background-color</span>CSS プロパティを透明に設定 <span class="codeph"> ます </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt-png-alpha`
