---
title: interactivedata
description: インタラクティブビデオビューアのURL コマンド。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f9f5aa7a-3e0a-434a-8623-b439c9b6f18b
TQID: 'https://experienceleague.adobe.com/xIjjnZZX0Y7wce2TJwN2R228elxxysj0qXB2WELq9xc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 4%

---

# interactivedata{#interactivedata}

インタラクティブビデオビューアのURL コマンド。

`interactivedata= *` ファイル `*`

インタラクティブデータは、ビデオコンテンツの特定の時間領域を、後でビデオの横にあるインタラクティブスウォッチに表示される製品データに関連付けます。 ビデオ再生の終了時に表示されるcall-to-action パネルにも関連付けられます。 また、call-to-action パネルに表示されるインタラクティブビデオのタイトルも提供されます。

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ファイル </span> </span> </p> </td> 
   <td colname="col2"> <p> WebVTT インタラクティブデータコンテンツのURLまたはパスを指定します。 WebVTT ファイルは、画像サービングで提供する必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

なし

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
interactivedata=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt
```
