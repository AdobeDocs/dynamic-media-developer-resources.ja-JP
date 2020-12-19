---
description: メイン表示は、カタログ画像で構成されます。 スワイプして別のページに移動したり、ズームしたりできます。
seo-description: メイン表示は、カタログ画像で構成されます。 スワイプして別のページに移動したり、ズームしたりできます。
seo-title: ページ表示
solution: Experience Manager
title: ページ表示
topic: Dynamic media
uuid: f585bf57-c66a-4213-a2af-d9625beb5bed
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 2%

---


# ページ表示{#page-view}

メイン表示は、カタログ画像で構成されます。 スワイプして別のページに移動したり、ズームしたりできます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

表示領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7pageview
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
   <td colname="col2"> <p> 16進数形式のメイン表示の背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor  </span> </p> </td> 
   <td colname="col2"> <p>メイン表示の上に表示されるカーソル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — メイン表示を透明にするには、次のように記述します。

```
.s7ecatalogsearchviewer .s7pageview { 
 background-color: transparent; 
}
```

デスクトップシステムでは、コンポーネントは`.s7pageview`クラスに適用できる`cursortype`属性セレクターをサポートし、コンポーネントの状態とユーザー操作に基づいてカーソルのタイプを制御します。 次の`cursortype`値がサポートされています。

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
   <td colname="col2"> <p>画像解像度が低い、コンポーネントの設定またはその両方が原因で画像がズーム可能でない場合に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin  </span> </p> </td> 
   <td colname="col2"> <p>画像がズームイン可能な場合に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> リセット </span> </p> </td> 
   <td colname="col2"> <p>画像が最大ズームレベルに達し、初期状態にリセット可能な場合に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ドラッグ </span> </p> </td> 
   <td colname="col2"> <p>ユーザーがズームイン状態の画像をパンした場合に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide  </span> </p> </td> 
   <td colname="col2"> <p>ユーザーが水平スワイプまたはフリックで画像の入れ替えを実行した場合に表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

カタログ見開きの左右のページを視覚的に区切るページ区切りは、以下のCSSクラスセレクターを使用して制御します。

`.s7ecatalogsearchviewer .s7pageview .s7pagedivider`

<table id="table_77EBC9A77BF14CF4974F8F43C709A207"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> ページ区切りの幅。 区切りを完全に非表示にするには、<span class="codeph"> 0 </span> pxに設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>ページ区切りとして使用する画像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 幅が40ピクセルで、半透明の画像を使用したページ区切りを設定します。

```
.s7ecatalogsearchviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>`frametransition`修飾子が`turn`または`auto`（デスクトップシステムの場合）に設定されている場合、ページ区切りの外観は`pageturnstyle`修飾子を使用して制御され、`.s7pagedivider` CSSクラスは無視されます。

メインビューア領域にカスタムのマウスカーソルを表示するよう設定できます。 これは、`.s7ecatalogsearchviewer .s7pageview` CSSクラスに適用される追加の属性セレクターを使用して制御します。

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> デフォルト </span> </p> </td> 
   <td colname="col2"> <p> 通常は矢印で、ズーム可能でない画像に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin  </span> </p> </td> 
   <td colname="col2"> <p> 画像がズームイン可能な場合に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> リセット </span> </p> </td> 
   <td colname="col2"> <p>画像が最大ズームに達し、リセット可能な場合に表示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ドラッグ </span> </p> </td> 
   <td colname="col2"> <p>ズームインされた画像に対してドラッグ操作を実行するときに表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide  </span> </p> </td> 
   <td colname="col2"> <p>ユーザーがスライドジェスチャを使用して画像の入れ替えを行うときに表示されます </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — コンポーネント状態のタイプごとに異なるマウスカーソルを設定します。

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

