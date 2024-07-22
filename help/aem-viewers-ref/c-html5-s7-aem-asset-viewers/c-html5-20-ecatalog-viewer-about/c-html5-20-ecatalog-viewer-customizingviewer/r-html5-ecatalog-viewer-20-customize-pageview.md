---
title: ページビュー
description: メインビューは、カタログ画像で構成されます。 スワイプして別のページに移動したり、ズームしたりできます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d3368115-15e7-4d9d-a417-a3c82c9a8a64
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 1%

---

# ページビュー{#page-view}

メインビューは、カタログ画像で構成されます。 スワイプして別のページに移動したり、ズームしたりできます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域の CSS プロパティ**

表示領域の外観は、次の CSS クラスセレクターで制御します。

```
.s7ecatalogviewer .s7pageview
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
   <td colname="col2"> <p> メインビューの背景色（16 進数形式）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>メイン ビューに表示されるカーソル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – メインビューを透明にする。

```
.s7ecatalogviewer .s7pageview { 
 background-color: transparent; 
}
```

デスクトップシステムでは、コンポーネントは、クラスに適用できる `cursortype` 属性セレクター `.s7pageview` サポートしており、コンポーネントの状態とユーザーアクションに基づいてカーソルのタイプを制御します。 次の `cursortype` 値がサポートされています。

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>値 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default </span> </p> </td> 
   <td colname="col2"> <p>画像の解像度が低い、コンポーネント設定がある、またはその両方が原因で画像をズームできない場合に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p>画像をズームインできる場合に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset </span> </p> </td> 
   <td colname="col2"> <p>画像が最大ズームレベルにあり、初期状態にリセットできる場合に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ドラッグ </span> </p> </td> 
   <td colname="col2"> <p>ズームイン状態の画像をユーザーがパンすると表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> スライド </span> </p> </td> 
   <td colname="col2"> <p>ユーザーが水平方向のスワイプまたはフリックを行って画像の入れ替えを実行すると表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

カタログスプレッドの左右のページを視覚的に区切るページディバイダーは、次の CSS クラスセレクターで制御します。

`.s7ecatalogviewer .s7pageview .s7pagedivider`

<table id="table_77EBC9A77BF14CF4974F8F43C709A207"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p> ページ区切りの幅。 ディバイダーを完全に非表示にするには、<span class="codeph"> 0 </span> px に設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>ページディバイダーとして使用する画像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 半透明の画像を持つ 40 ピクセルの幅のページディバイダーを持つこと。

```
.s7ecatalogviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>`frametransition` 修飾子が `turn` または `auto` （デスクトップシステム上）に設定されている場合、ページディバイダーの外観は `pageturnstyle` 修飾子で制御され、`.s7pagedivider` CSS クラスは無視されます。

メインビューア領域でのカスタムマウスカーソルの表示を設定できます。 この機能は、CSS クラスに適用された追加の属性セレクターで制御 `.s7ecatalogviewer .s7pageview` れます。

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default </span> </p> </td> 
   <td colname="col2"> <p> 通常、矢印はズームできない画像を示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p> 画像をズームインできるタイミングを表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset </span> </p> </td> 
   <td colname="col2"> <p>画像が最大ズーム時を示し、リセット可能です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ドラッグ </span> </p> </td> 
   <td colname="col2"> <p>ユーザーがズームインされた画像にドラッグ操作を実行すると表示されます </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> スライド </span> </p> </td> 
   <td colname="col2"> <p>ユーザーがスライド ジェスチャを使用して画像の入れ替えを実行したときに表示します </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – コンポーネントの状態のタイプごとに異なるマウスカーソルがある

```
.s7ecatalogviewer .s7pageview[cursortype="default"] { 
cursor:auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="zoomin"] { 
cursor:url(images/zoomin_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="reset"] { 
cursor:url(images/zoomout_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview [cursortype="slide"] { 
cursor:url(images/slide_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="drag"] { 
cursor:url(images/drag_cursor.cur), auto; 
}
```
