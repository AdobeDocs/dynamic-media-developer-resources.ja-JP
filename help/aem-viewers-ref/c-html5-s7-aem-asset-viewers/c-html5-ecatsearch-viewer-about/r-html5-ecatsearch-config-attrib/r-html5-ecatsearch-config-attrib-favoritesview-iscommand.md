---
description: すべてのサムネールに適用される画像サービングコマンド文字列。
seo-description: すべてのサムネールに適用される画像サービングコマンド文字列。
seo-title: お気に入りビュー.iscommand
solution: Experience Manager
title: お気に入りビュー.iscommand
topic: Dynamic media
uuid: be3d49d1-d5d2-4ecd-bc8f-fe5f80204c76
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# お気に入りビュー.iscommand{#favoritesview-iscommand}

すべてのサムネールに適用される画像サービングコマンド文字列。

[!DNL `[FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> URLで指定する場合、 <span class="codeph"> &amp;と=のすべての出現箇所を</span> %26 <span class="codeph"> と%3DのそれぞれにHTTPエンコードする</span><span class="codeph"></span><span class="codeph"></span>必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

なし

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

ビューアのURLで指定する場合。

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

configデータで指定する場合。

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
