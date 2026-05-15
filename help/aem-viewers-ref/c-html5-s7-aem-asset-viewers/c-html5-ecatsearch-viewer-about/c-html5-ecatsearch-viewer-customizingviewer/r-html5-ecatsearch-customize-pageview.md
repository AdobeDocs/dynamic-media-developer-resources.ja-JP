---
title: ページビュー
description: メインビューは、カタログ画像で構成されます。 スワイプして別のページに移動したり、ズームしたりできます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d98babad-96c7-419a-abf2-3b6657d550eb
TQID: 'https://experienceleague.adobe.com/IN5BJWNHvq-xzVmyu8gX-yIYCt-QvkgI3pvOp6nOP-Y'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 388
ht-degree: 1%

---

# ページビュー{#page-view}

メインビューは、カタログ画像で構成されます。 スワイプして別のページに移動したり、ズームしたりできます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

メイン ビューア領域の&#x200B;**CSS プロパティ**

表示領域の外観は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7pageview
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
   <td colname="col2"> <p> メインビューの背景色（16進数形式）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カーソル </span> </p> </td> 
   <td colname="col2"> <p>メインビュー上に表示されるカーソル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – メインビューを透明にします。

```
.s7ecatalogsearchviewer .s7pageview { 
 background-color: transparent; 
}
```

デスクトップシステムでは、コンポーネントは`.s7pageview` クラスに適用できる`cursortype`属性セレクターをサポートし、コンポーネントの状態とユーザーアクションに基づいてカーソルの種類を制御します。 次の`cursortype`値がサポートされています：

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>値 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> デフォルト </span> </p> </td> 
   <td colname="col2"> <p>画像の解像度が小さい、コンポーネント設定、またはその両方が原因で、画像がズームできない場合に表示されます。 </p> </td> 
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
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> スライド </span> </p> </td> 
   <td colname="col2"> <p>ユーザーが水平方向のスワイプまたはフリックを行って画像の入れ替えを実行したときに表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

カタログスプレッドの左右のページを視覚的に区切るページ区切りは、次のCSS クラスセレクターで制御されます。

`.s7ecatalogsearchviewer .s7pageview .s7pagedivider`

<table id="table_77EBC9A77BF14CF4974F8F43C709A207"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p> ページ区切りの幅。 ディバイダを完全に非表示にするには、<span class="codeph"> 0 </span> pxに設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p>ページディバイダとして使用する画像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 半透明の画像を含む幅40 ピクセルのページディバイダを作成します。

```
.s7ecatalogsearchviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>`frametransition`修飾子が`turn`または`auto`に設定されている場合（デスクトップシステムの場合）、ページディバイダの外観は`pageturnstyle`修飾子で制御され、`.s7pagedivider`CSS クラスは無視されます。

メインビューア領域の上にカスタムマウスカーソルを表示するように設定できます。 この機能は、`.s7ecatalogsearchviewer .s7pageview` CSS クラスに適用された追加の属性セレクターで制御されます。

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> デフォルト </span> </p> </td> 
   <td colname="col2"> <p> 通常は矢印が表示され、ズームできない画像が表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ズームイン </span> </p> </td> 
   <td colname="col2"> <p> 画像をズームインできるタイミングを表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">さんが</span>をリセットしました </p> </td> 
   <td colname="col2"> <p>画像のズームが最大で、リセット可能な場合に表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span>をドラッグ </p> </td> 
   <td colname="col2"> <p>ズームされた画像に対してユーザーがドラッグ操作を実行する場合に表示します </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> スライド </span> </p> </td> 
   <td colname="col2"> <p>ユーザーがスライドジェスチャーを使用して画像の入れ替えを実行する場合に表示します </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – コンポーネントの状態のタイプごとに異なるマウスカーソルを使用します。

```
.s7ecatalogsearchviewer .s7pageview[cursortype="default"] { 
cursor:auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="zoomin"] { 
cursor:url(images/zoomin_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="reset"] { 
cursor:url(images/zoomout_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview [cursortype="slide"] { 
cursor:url(images/slide_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="drag"] { 
cursor:url(images/drag_cursor.cur), auto; 
}
```
