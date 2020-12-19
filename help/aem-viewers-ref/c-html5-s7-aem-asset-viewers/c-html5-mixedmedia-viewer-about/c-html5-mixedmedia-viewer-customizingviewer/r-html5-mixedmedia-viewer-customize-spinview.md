---
description: 現在のアセットがスピンセットの場合、メイン表示はスピン画像で構成されます。
seo-description: 現在のアセットがスピンセットの場合、メイン表示はスピン画像で構成されます。
seo-title: スピン表示
solution: Experience Manager
title: スピン表示
topic: Dynamic media
uuid: f1edbcc4-966a-4ec6-8ba9-a76f3ae51733
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---


# スピン表示{#spin-view}

現在のアセットがスピンセットの場合、メイン表示はスピン画像で構成されます。

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
   <td colname="col2"> <p> スピン表示の16進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — スピン表示を透明にするには、次のように記述します。

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```

