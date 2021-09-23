---
title: interactivedata
description: インタラクティブビデオビューア用のURLコマンド。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f9f5aa7a-3e0a-434a-8623-b439c9b6f18b
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 6%

---

# interactivedata{#interactivedata}

インタラクティブビデオビューア用のURLコマンド。

`interactivedata= *`ファイル`*`

インタラクティブデータは、ビデオコンテンツ内の特定の時間領域を、後でビデオの隣のインタラクティブスウォッチに表示される製品データに関連付けます。 また、ビデオ再生の終了時に表示されるコールトゥアクションパネルにも関連付けられています。 また、コールトゥアクションパネルに表示されるインタラクティブビデオのタイトルも示します。

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file</span> </span> </p> </td> 
   <td colname="col2"> <p> WebVTTインタラクティブデータコンテンツのURLまたはパスを指定します。 WebVTTファイルは画像サービングから提供される必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

なし

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
interactivedata=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt
```
