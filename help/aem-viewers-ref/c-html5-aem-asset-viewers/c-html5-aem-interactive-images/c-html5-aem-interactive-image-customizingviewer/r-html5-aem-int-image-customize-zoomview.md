---
description: メインビューは静的な画像で構成されます。
solution: Experience Manager
title: ズームビュー
feature: Dynamic Media Classic，ビューア，SDK/API，インタラクティブ画像
role: Developer,User
exl-id: e83d53a1-bee9-4e4d-8295-a3a350f3ff9c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 1%

---

# ズームビュー{#zoom-view}

メインビューは静的な画像で構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

表示領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7interactiveimage .s7zoomview
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
   <td colname="col2"> <p> メインビューの16進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — メインビューを透明にするには、次のように記述します。

```
.s7interactiveimage .s7zoomview { 
 background-color: transparent; 
}
```
