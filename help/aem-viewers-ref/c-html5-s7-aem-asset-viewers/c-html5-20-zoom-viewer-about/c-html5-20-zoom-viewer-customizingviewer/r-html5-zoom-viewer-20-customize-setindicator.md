---
title: インジケーターを設定
description: セットインジケーターは、タッチデバイスでビューアを使用したときに、スウォッチの上にレンダリングされる一連のドットです。 ドットは、スクロールボタンが使用できない場合に、ユーザーがサムネールのページ間を移動するのに役立ちます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: b1e6734e-a341-45d7-b771-daeb0527cd00
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# インジケーターを設定{#set-indicator}

セットインジケーターは、タッチデバイスでビューアを使用したときに、スウォッチの上にレンダリングされる一連のドットです。 ドットは、スクロールボタンが使用できない場合に、ユーザーがサムネールのページ間を移動するのに役立ちます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**セットインジケーターの CSS プロパティ**

セットインジケーターコンテナの外観は、次の CSS クラスセレクターで制御します。

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
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>設定されたインジケーターの 16 進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 背景が白いセットインジケーターを作成するには：

```
.s7zoomviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

個々のセットインジケータードットの外観は、CSS クラスセレクターで制御します。

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
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>設定されたインジケータードットの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>設定されたインジケータードットの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p>左余白（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p>上マージン （ピクセル単位）。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>背景色（16 進数形式）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>セットインジケータードットは、`state` 属性セレクターをサポートしており、異なるサムネール状態に異なるスキンを適用するために使用できます。 特に、`state="selected"` は現在のサムネールのページに対応 `state="unselected"`、デフォルトのドット状態に対応します。

例 – セットインジケーターのドットを 15 x 15 ピクセルに設定し、水平方向の余白 2 ピクセル、上部の余白 5 ピクセル、下部の余白 1 ピクセル、半径 12 ピクセル、デフォルトの色#D5D3D3 アクティブな色#939393 使用するには：

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
