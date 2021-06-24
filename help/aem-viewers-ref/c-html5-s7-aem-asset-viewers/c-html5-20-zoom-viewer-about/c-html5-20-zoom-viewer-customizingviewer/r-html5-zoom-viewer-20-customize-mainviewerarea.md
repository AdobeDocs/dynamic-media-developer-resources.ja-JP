---
description: メインビュー領域は、ズーム画像とスウォッチが表示される領域です。 通常、サイズが指定されていない場合は、使用可能なデバイス画面に合わせてが設定されます。
solution: Experience Manager
title: メインビューア領域
feature: Dynamic Media Classic，ビューア，SDK/API，ズーム
role: Developer,Business Practitioner
exl-id: 62cbb3e6-e766-40a3-9c01-d22ade82b604
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 1%

---

# メインビューア領域{#main-viewer-area}

メインビュー領域は、ズーム画像とスウォッチが表示される領域です。 通常、サイズが指定されていない場合は、使用可能なデバイス画面に合わせてが設定されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

埋め込みモードで作業する場合（メインビューア領域に明示的なサイズを指定した場合）、ビューアは、単一の画像で作業しているスウォッチコンポーネントの高さだけメイン領域の高さを自動的に小さくするので、スウォッチは不要です。

**メインビューア領域のCSSプロパティ**

表示領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7zoomviewer
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ビューアの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ビューアの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 16進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 白の背景(`#FFFFFF`)のビューアを設定し、サイズを512 x 288ピクセルにするには、次のように記述します。

```
.s7zoomviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
