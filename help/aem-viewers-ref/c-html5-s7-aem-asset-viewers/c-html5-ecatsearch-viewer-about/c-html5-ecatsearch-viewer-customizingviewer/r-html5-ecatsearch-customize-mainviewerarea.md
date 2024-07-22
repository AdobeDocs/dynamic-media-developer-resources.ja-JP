---
title: メインビューア領域
description: メイン ビュー領域は、カタログ イメージが占める領域です。 通常、サイズが指定されていない場合は、デバイスの使用可能な画面に合わせて設定されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 854f5fa7-f46d-4c4f-9a44-886fec93f606
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# メインビューア領域{#main-viewer-area}

メイン ビュー領域は、カタログ イメージが占める領域です。 通常、サイズが指定されていない場合は、デバイスの使用可能な画面に合わせて設定されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域の CSS プロパティ**

表示領域の外観は、次の CSS クラスセレクターで制御します。

```
.s7ecatalogsearchviewer
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
.s7ecatalogsearchviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
