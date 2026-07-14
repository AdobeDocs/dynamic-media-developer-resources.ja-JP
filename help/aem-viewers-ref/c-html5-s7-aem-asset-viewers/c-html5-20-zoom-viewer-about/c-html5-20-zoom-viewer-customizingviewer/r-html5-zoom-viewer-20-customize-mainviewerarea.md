---
title: メインのビューアエリア
description: メインビュー領域は、ズーム画像とスウォッチが占める領域です。 通常、サイズが指定されていない場合は、使用可能なデバイス画面に合わせて設定されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 62cbb3e6-e766-40a3-9c01-d22ade82b604
TQID: 'https://experienceleague.adobe.com/mAfXI6eLoLmVR7yI6EvUjlVjQrQ8J86ikUZGa5rRN4E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 170
ht-degree: 0%

---

# メインのビューアエリア{#main-viewer-area}

メインビュー領域は、ズーム画像とスウォッチが占める領域です。 通常、サイズが指定されていない場合は、使用可能なデバイス画面に合わせて設定されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

埋め込みモードで作業する場合（メインビューア領域に明示的なサイズを指定する場合）、ビューアは、単一の画像を操作しているスウォッチコンポーネントの高さによってメインエリアの高さを自動的に下げるので、スウォッチは必要ありません。

メイン ビューア領域の&#x200B;**CSS プロパティ**

表示領域の外観は、次のCSS クラスセレクターで制御されます。

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
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>ビューアの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>ビューアの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 16進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 白い背景（`#FFFFFF`）のビューアを設定し、サイズを512 x 288 ピクセルにします。

```
.s7zoomviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

