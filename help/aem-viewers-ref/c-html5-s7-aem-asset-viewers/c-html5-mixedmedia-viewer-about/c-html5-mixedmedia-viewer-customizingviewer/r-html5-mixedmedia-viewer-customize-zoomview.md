---
title: ズーム表示
description: 連続ズームモードでは、現在のアセットが単一の画像の場合、メインビューはズーム可能な画像で構成されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0252436b-ba96-4273-b796-d1772fc093b0
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# ズーム表示{#zoom-view}

連続ズームモードでは、現在のアセットが単一の画像の場合、メインビューはズーム可能な画像で構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域の CSS プロパティ**

表示領域の外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7mixedmediaviewer .s7zoomview
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
   <td colname="col2"> <p> メインビューの 16 進数形式の背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カーソル </span> </p> </td> 
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

デスクトップシステムでは、コンポーネントは、 `cursortype` 属性セレクター `.s7zoomview` クラス。 コンポーネントの状態とユーザーの操作に基づいて、カーソルのタイプを制御します。 以下 `cursortype` の値はサポートされています。

* `default`

   画像の解像度が小さい、またはコンポーネントの設定、あるいはその両方の理由で画像がズームできない場合に表示されます。

* `zoomin`

   画像がズームイン可能な場合に表示されます。

* `reset`

   画像が最大ズームレベルで、初期状態にリセットできる場合に表示されます。

* `drag`

   ユーザーがズームイン状態の画像をパンしたときに表示されます。

* `slide`

   ユーザーが水平方向のスワイプまたはフリックを実行して画像の入れ替えを実行した場合に表示されます。
