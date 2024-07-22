---
title: メインビューア領域
description: メイン ビューエリアは、メイン ビューとスウォッチが占めるエリアです。 サイズが指定されていない場合、使用可能なデバイス画面に合わせて設定されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: fe8b748c-5318-4fcd-9f3a-d50523bb3f8f
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# メインビューア領域{#main-viewer-area}

メイン ビューエリアは、メイン ビューとスウォッチが占めるエリアです。 サイズが指定されていない場合、使用可能なデバイス画面に合わせて設定されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域の CSS プロパティ**

表示領域の外観は、次の CSS クラスセレクターで制御します。

```
.s7mixedmediaviewer 
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
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ビューアの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ビューアの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p> 背景色（16 進数形式）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 白い背景（`#FFFFFF`）を持つビューアを設定し、そのサイズを 512 x 288 ピクセルにする

```
.s7mixedmediaviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
