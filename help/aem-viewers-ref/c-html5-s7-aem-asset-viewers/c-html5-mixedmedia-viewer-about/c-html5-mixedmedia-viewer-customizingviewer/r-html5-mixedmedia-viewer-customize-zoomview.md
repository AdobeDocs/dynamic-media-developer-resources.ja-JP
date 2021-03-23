---
description: 連続ズームモードでは、現在のアセットが単一の表示の場合、メイン画像はズーム可能な画像で構成されます。
seo-description: 連続ズームモードでは、現在のアセットが単一の表示の場合、メイン画像はズーム可能な画像で構成されます。
seo-title: ズーム表示
solution: Experience Manager
title: ズーム表示
uuid: c9113275-eec6-4014-b7ad-3ae9f2cf01d9
feature: Dynamic Mediaクラシック，ビューア，SDK/API，混在メディアセット
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---


# ズーム表示{#zoom-view}

連続ズームモードでは、現在のアセットが単一の表示の場合、メイン画像はズーム可能な画像で構成されます。

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
   <td colname="col2"> <p> メイン表示の16進数形式の背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor  </span> </p> </td> 
   <td colname="col2"> <p>メイン表示上に表示されるカーソル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — ズーム表示を透明にするには、次のように記述します。

```
.s7mixedmediaviewer .s7zoomview { 
 background-color: transparent; 
}
```

デスクトップシステムでは、コンポーネントは`cursortype`属性セレクターをサポートします。このセレクターは`.s7zoomview`クラスに適用できます。 コンポーネントの状態とユーザー操作に基づいて、カーソルの種類を制御します。 次の`cursortype`値がサポートされています。

* `default`

   画像解像度が低い、コンポーネントの設定、またはその両方が原因で画像がズーム可能でない場合に表示されます。

* `zoomin`

   画像がズームイン可能な場合に表示されます。

* `reset`

   画像が最大ズームレベルに達し、初期状態にリセット可能な場合に表示されます。

* `drag`

   ユーザーがズームイン状態の画像をパンした場合に表示されます。

* `slide`

   ユーザーが水平スワイプまたはフリックで画像の入れ替えを実行した場合に表示されます。

