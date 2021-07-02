---
description: 現在のアセットがスピンセットの場合、メインビューはスピン画像で構成されます。
solution: Experience Manager
title: スピンビュー
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,Business Practitioner
exl-id: aafc1299-b09a-4379-bd8f-b564066175bd
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 1%

---

# スピンビュー{#spin-view}

現在のアセットがスピンセットの場合、メインビューはスピン画像で構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

表示領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7mixedmediaviewer .s7spinview
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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> スピンビューの16進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — スピンビューを透明にするには、次のように記述します。

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```
