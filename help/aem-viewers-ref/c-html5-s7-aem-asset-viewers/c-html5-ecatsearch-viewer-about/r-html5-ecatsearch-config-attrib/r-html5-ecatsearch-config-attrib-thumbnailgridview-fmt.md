---
description: ThumbnailGridView.fmt
solution: Experience Manager
title: ThumbnailGridView.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ff57762e-05f5-41c1-956f-39280941eeb1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 4%

---

# ThumbnailGridView.fmt{#thumbnailgridview-fmt}

[!DNL `[ThumbnailGridView.|<containerId>_gridView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>コンポーネントが Image Server から画像を読み込むために使用する画像形式を指定します。 Image Server とクライアントブラウザーがサポートする任意の値を指定できます。 指定した形式が – alpha<span class="codeph"> で終わ </span> 場合、コンポーネントは画像を透明コンテンツとしてレンダリングします。 他のすべての画像形式では、コンポーネントは画像を不透明として扱います。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-ffe8ccc3a5f2474db47a68c2ad9a96d6}

オプション。

## 初期設定 {#section-502c098dbae1452180c7f575a1d9dc8b}

[!DNL `jpeg`]

## 例 {#section-5cde7b856ba646c293cfd3d79e47c507}

[!DNL `fmt-png-alpha`]
