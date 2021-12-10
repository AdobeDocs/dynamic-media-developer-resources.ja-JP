---
title: 指標を設定
description: セットインジケーターは、タッチデバイスでビューアを使用したときにスウォッチの上にレンダリングされる一連のドットです。 ドットは、スクロールボタンを使用できない場合に、サムネールのページ間を移動するのに役立ちます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: b1e6734e-a341-45d7-b771-daeb0527cd00
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 指標を設定{#set-indicator}

セットインジケーターは、タッチデバイスでビューアを使用したときにスウォッチの上にレンダリングされる一連のドットです。 ドットは、スクロールボタンを使用できない場合に、サムネールのページ間を移動するのに役立ちます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**設定インジケーターの CSS プロパティ**

設定インジケーターコンテナの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7zoomviewer .s7setindicator
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
   <td colname="col2"> <p>設定インジケーターの 16 進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 背景が白の設定インジケーターを作成するには：

```
.s7zoomviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

個々のセットインジケーターのドットの外観は、CSS クラスセレクターを使用して制御します。

`.s7zoomviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>設定インジケーターのドットの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>設定インジケーターのドットの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p>左余白（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p>上余白（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right </span> </p> </td> 
   <td colname="col2"> <p>右余白（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-bottom </span> </p> </td> 
   <td colname="col2"> <p>下余白（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>境界線の半径（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>16 進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>インジケーターのドットを設定すると、 `state` 属性セレクター。サムネールの状態ごとに異なるスキンを適用するのに使用できます。 特に `state="selected"` は、現在のサムネールのページに対応します。 `state="unselected"` は、デフォルトのドットの状態に対応します。

例 — 15 x 15 ピクセルで、2 ピクセルの水平マージン、5 ピクセルの上マージン、1 ピクセルの下マージン、12 ピクセルの半径、#D5D3D3 default color および#939393アクティブな色の設定インジケーターのドットを作成するには、次のように記述します。

```
.s7zoomviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7zoomviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```
