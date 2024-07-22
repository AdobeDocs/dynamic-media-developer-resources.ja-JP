---
title: メインビューア領域
description: メイン表示領域は、ズーム画像とスウォッチが占める領域です。 通常、サイズが指定されていない場合は、デバイスの使用可能な画面に合わせて設定されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 62cbb3e6-e766-40a3-9c01-d22ade82b604
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# メインビューア領域{#main-viewer-area}

メイン表示領域は、ズーム画像とスウォッチが占める領域です。 通常、サイズが指定されていない場合は、デバイスの使用可能な画面に合わせて設定されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

埋め込みモードで作業している場合（メインビューア領域に明示的なサイズが指定されている場合）、ビューアは、単一画像で作業しているスウォッチコンポーネントの高さだけメイン領域の高さを自動的に下げるので、スウォッチは必要ありません。

**メインビューア領域の CSS プロパティ**

表示領域の外観は、次の CSS クラスセレクターで制御します。

```
.s7zoomviewer
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
.s7zoomviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
