---
description: すべてのサムネールに適用される画像サービングコマンド文字列。
solution: Experience Manager
title: FavoritesView.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 114cc5b7-32b9-4d16-ab93-a66f3ec666e0
TQID: 'https://experienceleague.adobe.com/FZZjN7PhDctqlyEfwrp-25xrCJ5tYeklalzZtMyeIns'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 61
ht-degree: 6%

---

# FavoritesView.iscommand{#favoritesview-iscommand}

すべてのサムネールに適用される画像サービングコマンド文字列。

[!DNL `[FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> URLで指定した場合、<span class="codeph"> &amp;</span>および<span class="codeph"> =</span>のすべての出現箇所は、それぞれ<span class="codeph"> %26</span>および<span class="codeph"> %3D</span>としてHTTP エンコードする必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

なし

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

ビューア URLで指定した場合。

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

設定データで指定すると。

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
