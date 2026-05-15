---
title: ズームビュー
description: メインビューは、ズーム可能な画像で構成されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 286b9df4-88db-4e5d-aab4-9cbe01195e57
TQID: 'https://experienceleague.adobe.com/ub5sNABbFHA-V5yaiNmUAHZ1NwTGIlzNecIL5KlJPg4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 165
ht-degree: 1%

---

# ズームビュー{#zoom-view}

メインビューは、ズーム可能な画像で構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

メイン ビューア領域の&#x200B;**CSS プロパティ**

表示領域の外観は、次のCSS クラスセレクターで制御されます。

```
.s7basiczoomviewer .s7zoomview
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
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> メインビューの16進数形式の背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カーソル </span> </p> </td> 
   <td colname="col2"> <p>カーソルはメインビューの上に表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – メインビューを透明にします。

```
.s7basiczoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

デスクトップシステムでは、コンポーネントは`.s7zoomview` クラスに適用できる`cursortype`属性セレクターをサポートし、コンポーネントの状態とユーザーアクションに基づいてカーソルの種類を制御します。 次の`cursortype`値がサポートされています：

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
   <td colname="col2"> <p>画像の解像度が小さい場合、またはコンポーネントの設定が原因で画像がズームできない場合、またはその両方が表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ズームイン </span> </p> </td> 
   <td colname="col2"> <p>画像をズームインできる場合に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">さんが</span>をリセットしました </p> </td> 
   <td colname="col2"> <p>画像が最大ズームレベルで、初期状態にリセットできる場合に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span>をドラッグ </p> </td> 
   <td colname="col2"> <p>ユーザーがズームイン状態の画像をパンしたときに表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>
