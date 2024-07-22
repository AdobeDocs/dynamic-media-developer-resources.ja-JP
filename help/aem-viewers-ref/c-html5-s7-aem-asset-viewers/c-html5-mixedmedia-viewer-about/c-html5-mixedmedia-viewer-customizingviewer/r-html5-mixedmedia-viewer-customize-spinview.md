---
title: スピンビュー
description: メインビューは、現在のアセットがスピンセットの場合のスピン画像で構成されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: aafc1299-b09a-4379-bd8f-b564066175bd
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 1%

---

# スピンビュー{#spin-view}

メインビューは、現在のアセットがスピンセットの場合のスピン画像で構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域の CSS プロパティ**

表示領域の外観は、次の CSS クラスセレクターで制御します。

```
.s7mixedmediaviewer .s7spinview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p> スピンビューの 16 進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – スピンビューを透明にする。

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```
