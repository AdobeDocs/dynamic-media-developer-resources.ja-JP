---
title: FavoritesView.fmt
description: FavoritesView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d14f8a0c-5fb5-4315-ba8b-79add6d389b0
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# FavoritesView.fmt{#favoritesview-fmt}

`[FavoritesView.|<containerId>_favoritesView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> コンポーネントで Image Server から画像を読み込む際に使用する画像形式を指定します。 形式は、Image Server とクライアントブラウザーでサポートされる任意の値です。 </p> <p>画像形式が <span class="codeph"> -alpha</span>を指定した場合、コンポーネントは画像を透明なコンテンツとしてレンダリングします。 その他のすべての画像形式の値では、画像は不透明として扱われます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`jpeg`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`fmt=png-alpha`
