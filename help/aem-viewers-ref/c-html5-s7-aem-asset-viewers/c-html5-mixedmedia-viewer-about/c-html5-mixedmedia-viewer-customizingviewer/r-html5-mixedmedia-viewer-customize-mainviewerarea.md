---
description: メインビュー領域は、メインビューとスウォッチが表示される領域です。 サイズが指定されていない場合は、通常、使用可能なデバイス画面に収まるように設定されます。
solution: Experience Manager
title: メインビューア領域
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,Business Practitioner
exl-id: fe8b748c-5318-4fcd-9f3a-d50523bb3f8f
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 2%

---

# メインビューア領域{#main-viewer-area}

メインビュー領域は、メインビューとスウォッチが表示される領域です。 サイズが指定されていない場合は、通常、使用可能なデバイス画面に収まるように設定されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

表示領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7mixedmediaviewer 
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
.s7mixedmediaviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
