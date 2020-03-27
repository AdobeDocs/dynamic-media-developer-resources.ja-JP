---
description: 現在のアセットがスピンセットの場合、メインビューはスピン画像で構成されます。
seo-description: 現在のアセットがスピンセットの場合、メインビューはスピン画像で構成されます。
seo-title: スピンビュー
solution: Experience Manager
title: スピンビュー
topic: Dynamic media
uuid: f1edbcc4-966a-4ec6-8ba9-a76f3ae51733
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Spin view{#spin-view}

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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
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

