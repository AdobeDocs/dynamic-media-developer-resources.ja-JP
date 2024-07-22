---
description: すべてのサムネイルに適用される画像サービングコマンド文字列。
solution: Experience Manager
title: FavoritesView.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 114cc5b7-32b9-4d16-ab93-a66f3ec666e0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 6%

---

# FavoritesView.iscommand{#favoritesview-iscommand}

すべてのサムネイルに適用される画像サービングコマンド文字列。

[!DNL `[FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> URL で指定されている場合、<span class="codeph"> &amp;</span> および <span class="codeph"> =</span> は、それぞれ <span class="codeph"> %26</span> および <span class="codeph"> %3D</span> として HTTP エンコードする必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

なし

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

ビューアの URL で指定された場合。

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

設定データで指定された場合。

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
