---
description: 連続ズームモードでは、現在のアセットが単一の画像の場合、メインビューはズーム可能な画像で構成されます。
solution: Experience Manager
title: ズームビュー
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,User
exl-id: 0252436b-ba96-4273-b796-d1772fc093b0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# ズームビュー{#zoom-view}

連続ズームモードでは、現在のアセットが単一の画像の場合、メインビューはズーム可能な画像で構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

表示領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7mixedmediaviewer .s7zoomview
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
   <td colname="col2"> <p>メインビュー上に表示されるカーソル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — ズームビューを透明にするには、次のように記述します。

```
.s7mixedmediaviewer .s7zoomview { 
 background-color: transparent; 
}
```

デスクトップシステムでは、コンポーネントは`cursortype`属性セレクターをサポートし、`.s7zoomview`クラスに適用できます。 コンポーネントの状態とユーザーアクションに基づいて、カーソルのタイプを制御します。 次の`cursortype`値がサポートされています。

* `default`

   画像の解像度が小さい、またはコンポーネントの設定、あるいはその両方が原因で画像がズーム可能でない場合に表示されます。

* `zoomin`

   画像がズームイン可能な場合に表示されます。

* `reset`

   画像が最大ズームレベルで、初期状態にリセット可能な場合に表示されます。

* `drag`

   ユーザーがズームイン状態の画像をパンしたときに表示されます。

* `slide`

   ユーザーが水平方向のスワイプまたはフリックを実行して画像の入れ替えを実行した場合に表示されます。
