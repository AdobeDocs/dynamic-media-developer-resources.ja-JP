---
description: メインビューは、カタログ画像で構成されます。 スワイプして別のページに移動したり、ズームしたりできます。
seo-description: メインビューは、カタログ画像で構成されます。 スワイプして別のページに移動したり、ズームしたりできます。
seo-title: ページビュー
solution: Experience Manager
title: ページビュー
topic: Dynamic media
uuid: 5e247f56-f0da-487b-8e03-587b9d36aa39
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Page view{#page-view}

メインビューは、カタログ画像で構成されます。 スワイプして別のページに移動したり、ズームしたりできます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

表示領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7pageview
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
   <td colname="col2"> <p> 16進数形式のメインビューの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>メインビューの上に表示されるカーソル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — メインビューを透明にするには、次のように記述します。

```
.s7ecatalogviewer .s7pageview { 
 background-color: transparent; 
}
```

デスクトップシステムでは、コンポーネン `cursortype` トは、クラスに適用できる属性セレクターをサ `.s7pageview` ポートし、コンポーネントの状態とユーザーアクションに基づいてカーソルのタイプを制御します。 The following `cursortype` values are supported:

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
   <td colname="col2"> <p>画像の解像度が小さい、コンポーネントの設定、またはその両方が原因で画像がズーム可能でない場合に表示されます。 </p> </td> 
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
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide </span> </p> </td> 
   <td colname="col2"> <p>ユーザーが水平スワイプまたはフリックで画像の入れ替えを実行した場合に表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

カタログ見開きの左右のページを視覚的に区切るページ区切りは、以下のCSSクラスセレクターを使用して制御します。

`.s7ecatalogviewer .s7pageview .s7pagedivider`

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
   <td colname="col2"> <p> ページ区切りの幅。 区切りを完全 <span class="codeph"> に非表示にする </span> には、0ピクセルに設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>ページ区切りとして使用する画像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 幅が40ピクセルで、半透明の画像を使用するページ区切りを設定します。

```
.s7ecatalogviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>修飾子をま `frametransition` たはに設定 `turn` する `auto` と（デスクトップシステムで）、ページ区切りの外観は修飾子で制御され、 `pageturnstyle``.s7pagedivider` CSSクラスは無視されます。

メインビューア領域にカスタムのマウスカーソルを表示するように設定できます。 これは、 `.s7ecatalogviewer .s7pageview` CSSクラスに適用される追加の属性セレクターを使用して制御します。

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
   <td colname="col2"> <p> 通常は矢印で、ズーム可能でない画像に対して表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p> 画像がズームイン可能な場合に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> リセット </span> </p> </td> 
   <td colname="col2"> <p>画像が最大ズームに達し、リセット可能な場合に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ドラッグ </span> </p> </td> 
   <td colname="col2"> <p>ズームインされた画像に対してドラッグ操作を実行するときに表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide </span> </p> </td> 
   <td colname="col2"> <p>ユーザがスライドジェスチャを使用して画像の入れ替えを実行するときに表示 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — コンポーネントの状態のタイプごとに異なるマウスカーソルを使用します。

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

