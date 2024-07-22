---
title: メインビューア領域
description: メインの表示領域は、インタラクティブなスウォッチが占める領域です。 サイズが指定されていない場合、使用可能なデバイス画面に合わせて設定されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 8e5a44fa-422f-46f3-bd85-86bd2ce03899
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 1%

---

# メインビューア領域{#main-viewer-area}

メインの表示領域は、インタラクティブなスウォッチが占める領域です。 サイズが指定されていない場合、使用可能なデバイス画面に合わせて設定されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域の CSS プロパティ**

表示領域の外観は、次の CSS クラスセレクターで制御します。

```
.s7interactivevideoviewer
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

## 例 {#section-ee18025b182a42dc98052de5f133ddfe}

背景が白いビューアを設定し（`#FFFFFF`）、そのサイズを 512 x 288 ピクセルにするには

```
.s7interactivevideoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
