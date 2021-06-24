---
description: メインビュー領域は、カタログ画像が表示される領域です。 通常、サイズが指定されていない場合は、使用可能なデバイス画面に合わせてが設定されます。
solution: Experience Manager
title: メインビューア領域
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: 9a37936b-ee3d-4ea0-9a86-ea14d0ef8be9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# メインビューア領域{#main-viewer-area}

メインビュー領域は、カタログ画像が表示される領域です。 通常、サイズが指定されていない場合は、使用可能なデバイス画面に合わせてが設定されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

表示領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer
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
.s7ecatalogviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
