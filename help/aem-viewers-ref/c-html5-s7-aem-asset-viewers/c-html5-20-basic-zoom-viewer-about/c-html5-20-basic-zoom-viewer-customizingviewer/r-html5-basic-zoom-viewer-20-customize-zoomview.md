---
description: メインビューは、ズーム可能な画像で構成されます。
solution: Experience Manager
title: ズームビュー
feature: Dynamic Media Classic，ビューア，SDK/API，ズーム
role: Developer,Business Practitioner
exl-id: 286b9df4-88db-4e5d-aab4-9cbe01195e57
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 3%

---

# ズームビュー{#zoom-view}

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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> メインビューの16進数形式の背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor  </span> </p> </td> 
   <td colname="col2"> <p>カーソルがメインビュー上に表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — メインビューを透明にするには、次のように記述します。

```
.s7basiczoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

デスクトップシステムでは、コンポーネントは`cursortype`属性セレクターをサポートします。このセレクターは`.s7zoomview`クラスに適用でき、コンポーネントの状態とユーザー操作に基づいてカーソルの種類を制御します。 次の`cursortype`値がサポートされています。

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
   <td colname="col2"> <p>画像の解像度が小さい、またはコンポーネントの設定、あるいはその両方が原因で画像がズーム可能でない場合に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin  </span> </p> </td> 
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
