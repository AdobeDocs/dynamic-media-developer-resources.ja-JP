---
description: メイン表示は、バナーの画像で構成されます。
solution: Experience Manager
title: カルーセル表示
feature: Dynamic Mediaクラシック，ビューア，SDK/API，カルーセルバナー
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 1%

---


# カルーセル表示{#carousel-view}

メイン表示は、バナーの画像で構成されます。

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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> メイン表示の16進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — メイン表示を透明にするには、次のように記述します。

```
.s7carouselviewer .s7carouselview { 
 background-color: transparent; 
}
```

