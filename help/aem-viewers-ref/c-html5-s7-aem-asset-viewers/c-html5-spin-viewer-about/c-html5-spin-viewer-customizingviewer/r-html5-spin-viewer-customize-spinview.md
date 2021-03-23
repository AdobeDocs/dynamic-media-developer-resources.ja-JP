---
description: メイン表示は、スピン画像で構成されます。
seo-description: メイン表示は、スピン画像で構成されます。
seo-title: スピン表示
solution: Experience Manager
title: スピン表示
uuid: 74f42373-b08c-43c8-8f08-e61a09655b61
feature: Dynamic Mediaクラシック，ビューア，SDK/API，スピンセット
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 1%

---


# スピン表示{#spin-view}

メイン表示は、スピン画像で構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

表示領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7spinviewer .s7spinview
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
.s7spinviewer .s7spinview { 
 background-color: transparent; 
}
```

