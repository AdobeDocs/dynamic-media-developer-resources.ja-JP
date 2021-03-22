---
description: すべてのサムネールに適用される画像サービングコマンド文字列です。
seo-description: すべてのサムネールに適用される画像サービングコマンド文字列です。
seo-title: FavoritesView.iscommand
solution: Experience Manager
title: FavoritesView.iscommand
uuid: 59a25b65-a08f-46e9-a9eb-33672e4a0cb5
feature: Dynamic Mediaクラシック，ビューア，SDK/API,eCatalog
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 6%

---


# FavoritesView.iscommand{#favoritesview-iscommand}

すべてのサムネールに適用される画像サービングコマンド文字列です。

` [FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> URLで指定する場合、すべての<span class="codeph"> &amp;</span>および<span class="codeph"> =</span>を<span class="codeph"> %26</span>および<span class="codeph"> %3D</span>としてHTTPエンコードする必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

なし

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

ビューアのURLで指定する場合。

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

configデータで指定する場合。

`iscommand=op_sharpen=1&op_colorize=0xff0000`
