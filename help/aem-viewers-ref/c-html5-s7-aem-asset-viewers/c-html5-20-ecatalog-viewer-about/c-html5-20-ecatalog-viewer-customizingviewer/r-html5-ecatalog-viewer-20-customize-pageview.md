---
title: ページビュー
description: メインビューは、カタログ画像で構成されます。 スワイプして別のページに移動したり、ズームしたりできます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d3368115-15e7-4d9d-a417-a3c82c9a8a64
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 3%

---

# ページビュー{#page-view}

メインビューは、カタログ画像で構成されます。 スワイプして別のページに移動したり、ズームしたりできます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域の CSS プロパティ**

表示領域の外観は、以下の CSS クラスセレクターを使用して制御します。

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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 16 進数形式のメインビューの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カーソル </span> </p> </td> 
   <td colname="col2"> <p>メインビュー上に表示されるカーソル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — メインビューを透明にするには、次のように記述します。

```
.s7ecatalogviewer .s7pageview { 
 background-color: transparent; 
}
```

デスクトップシステムでは、コンポーネントは、 `cursortype` 適用可能な属性セレクター `.s7pageview` クラスを参照し、コンポーネントの状態とユーザーアクションに基づいて、カーソルのタイプを制御します。 以下 `cursortype` の値はサポートされています。

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
   <td colname="col2"> <p>画像の解像度が小さい、コンポーネントの設定、またはその両方の理由で画像がズームできない場合に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p>画像がズームイン可能な場合に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> リセット </span> </p> </td> 
   <td colname="col2"> <p>画像が最大ズームレベルで、初期状態にリセットできる場合に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ドラッグ </span> </p> </td> 
   <td colname="col2"> <p>ユーザーがズームイン状態の画像をパンしたときに表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> スライド </span> </p> </td> 
   <td colname="col2"> <p>ユーザーが水平方向のスワイプまたはフリックを実行して画像の入れ替えを実行した場合に表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

カタログ見開きの左右のページを視覚的に区切るページ区切りは、以下の CSS クラスセレクターを使用して制御します。

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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> ページ区切りの幅。 に設定 <span class="codeph"> 0 </span> px を指定すると、区切りが完全に非表示になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>ページ区切りとして使用する画像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 幅が 40 ピクセルで、半透明の画像を含むページ区切りを使用する場合。

```
.s7ecatalogviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>次の場合に `frametransition` 修飾子が次の値に設定されている `turn` または `auto` （デスクトップシステムの場合）ページ区切りの外観は、 `pageturnstyle` 修飾子と `.s7pagedivider` CSS クラスは無視されます。

メインビューア領域上でのカスタムマウスカーソルの表示を設定できます。 この機能は、 `.s7ecatalogviewer .s7pageview` CSS クラス：

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
   <td colname="col2"> <p> 通常は矢印で、ズーム不可の画像に対して表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p> いつ画像がズームインできるかを表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> リセット </span> </p> </td> 
   <td colname="col2"> <p>画像が最大ズームに達し、リセット可能な場合に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ドラッグ </span> </p> </td> 
   <td colname="col2"> <p>ユーザーがズームインされた画像に対してドラッグ操作を実行したときに表示されます </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> スライド </span> </p> </td> 
   <td colname="col2"> <p>ユーザーがスライドジェスチャを使用して画像の入れ替えを実行したときに表示されます </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — コンポーネントの状態のタイプごとに異なるマウスカーソルを持ちます。

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
