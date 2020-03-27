---
description: メインビューは、ズーム可能な画像で構成されます。
seo-description: メインビューは、ズーム可能な画像で構成されます。
seo-title: ズームビュー
solution: Experience Manager
title: ズームビュー
topic: Dynamic media
uuid: 06464e36-8c9c-4d3c-b4e5-5911f002568c
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Zoom view{#zoom-view}

メインビューは、ズーム可能な画像で構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

表示領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7basiczoomviewer .s7zoomview
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
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>カーソルがメインビューの上に表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — メインビューを透明にするには、次のように記述します。

```
.s7basiczoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

デスクトップシステムでは、コンポーネン `cursortype` トは、クラスに適用できる属性セレクターをサポートし、コ `.s7zoomview` ンポーネントの状態とユーザーアクションに基づいてカーソルのタイプを制御します。 The following `cursortype` values are supported:

<table id="table_BC9FC40DA27B4A85995F4E9431AABF33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>値 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> デフォルト </span> </p> </td> 
   <td colname="col2"> <p>画像の解像度が低い、またはコンポーネントの設定、あるいはその両方が原因で画像がズーム可能でない場合に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p>画像がズームイン可能な場合に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> リセット </span> </p> </td> 
   <td colname="col2"> <p>画像が最大ズームレベルで、初期状態にリセット可能な場合に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ドラッグ </span> </p> </td> 
   <td colname="col2"> <p>ユーザーがズームイン状態の画像をパンしたときに表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

