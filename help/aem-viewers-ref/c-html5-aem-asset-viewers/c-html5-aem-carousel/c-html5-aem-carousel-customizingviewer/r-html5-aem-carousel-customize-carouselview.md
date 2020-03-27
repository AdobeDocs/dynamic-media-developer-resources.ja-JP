---
description: メインビューは、バナーの画像で構成されます。
seo-description: メインビューは、バナーの画像で構成されます。
seo-title: カルーセルビュー
solution: Experience Manager
title: カルーセルビュー
topic: Dynamic media
uuid: bf2065cc-fef2-4d4e-ab2a-a533fa063a80
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# カルーセルビュー{#carousel-view}

メインビューは、バナーの画像で構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

表示領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7carouselviewer .s7carouselview
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> メインビューの16進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — メインビューを透明にするには、次のように記述します。

```
.s7carouselviewer .s7carouselview { 
 background-color: transparent; 
}
```

