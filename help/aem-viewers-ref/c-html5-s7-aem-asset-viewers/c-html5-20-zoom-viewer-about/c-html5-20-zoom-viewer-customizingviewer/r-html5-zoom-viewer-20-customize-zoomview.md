---
title: ズームビュー
description: メインビューは、ズーム可能な画像で構成されています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ae6c7f6f-5d71-49b5-adbb-782520961acf
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# ズームビュー{#zoom-view}

メインビューは、ズーム可能な画像で構成されています。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域の CSS プロパティ**

表示領域の外観は、次の CSS クラスセレクターで制御します。

```
.s7zoomviewer .s7zoomview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p> メインビューの 16 進数形式の背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>メインビューの上にカーソルが表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – メインビューを透明にする。

```
.s7zoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

デスクトップシステムでは、コンポーネントは `cursortype``.s7zoomview` クラスに適用できる属性セレクターをサポートしています。 コンポーネントの状態とユーザーの操作に基づいて、カーソルのタイプを制御します。 次の `cursortype` 値がサポートされています。

* `default`

  画像の解像度、コンポーネント設定、またはその両方が小さいために画像をズームできない場合に表示されます。

* `zoomin`

  画像をズームインできる場合に表示されます。

* `reset`

  画像が最大ズームレベルにあり、初期状態にリセットできる場合に表示されます。

* `drag`

  ズームイン状態の画像をユーザーがパンすると表示されます。

* `slide`

  ユーザーが水平スワイプまたはフリックを行って画像の入れ替えを実行すると表示されます。
