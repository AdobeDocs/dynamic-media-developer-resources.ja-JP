---
description: メインビュー領域は、ズーム画像が表示される領域です。 通常、サイズが指定されていない場合は、使用可能なデバイス画面に合わせてが設定されます。
solution: Experience Manager
title: メインビューア領域
feature: Dynamic Media Classic，ビューア，SDK/API，ズーム
role: Developer,User
exl-id: f51de2d6-0de2-4a4d-bbf4-185547e6c550
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 2%

---

# メインビューア領域{#main-viewer-area}

メインビュー領域は、ズーム画像が表示される領域です。 通常、サイズが指定されていない場合は、使用可能なデバイス画面に合わせてが設定されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

表示領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7basiczoomviewer
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
.s7basiczoomviewer{ 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
