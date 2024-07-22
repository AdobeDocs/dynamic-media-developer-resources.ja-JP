---
title: インジケーターを設定
description: セットインジケーターは、ビューアの下部にレンダリングされる一連のドットです。 セット内の現在の位置が表示されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 7d0827c5-f420-4804-983c-5298ee92b276
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---

# インジケーターを設定{#set-indicator}

セットインジケーターは、ビューアの下部にレンダリングされる一連のドットです。 セット内の現在の位置が表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**セットインジケーターの CSS プロパティ**

セットインジケーターコンテナの外観は、次の CSS クラスセレクターで制御します。

```
.s7carouselviewer .s7setindicator
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

>[!NOTE]
>
>セットインジケーターは、点線と数値の操作モードに異なるスタイルを適用するために使用できるモード属性セレクターをサポートしています。 特に、`mode="numeric"` は数値操作モードに対応し、`mode="dotted"` はデフォルトのドット状態に対応します。

例えば、背景が白いセットインジケーターを設定するとします。

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

個々のセットインジケータードットの外観は、CSS クラスセレクターで制御します。 点線と数値の両方の操作モードの項目に適用されます。

`.s7carouselviewer .s7setindicator .s7dot`

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
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>フォントの名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントのサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>フォントの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 垂直方向の位置揃え </span> </p> </td> 
   <td colname="col2"> <p>バナーインデックスの垂直方向揃え。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>バナーインデックスのテキストの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>セットインジケーター項目は `state` 属性セレクターをサポートしており、これを使用して、異なるスキンを異なるサムネール状態に適用できます。 特に、`state="selected"` はセット内の現在の要素に対応し、`state="unselected"` はデフォルトの項目状態に対応します。

例えば、デスクトップシステムでセットインジケーターを点線モードで設定するとします。 ビューアの下部から 20 ピクセルの位置に挿入します。 また、選択していないドットを 50% の透明度で黒に、7 ピクセルの角を丸めた 15 x 15 ピクセルにする必要があります。 選択されたドットは、透明度が 90% の黒、角が 9 ピクセルの丸い 18 x 18 ピクセルです。 ドットの間隔は 5 ピクセルです。

```
.s7carouselviewer.s7mouseinput .s7setindicator { 
 bottom: 20px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot{ 
 width:15px; 
 height:15px; 
 margin-left:2.5px; 
 margin-right:2.5px; 
 margin-top:2.5px; 
 margin-bottom:2.5px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='selected'] {  
 width:18px; 
 height:18px; 
 background-color: #000000; 
 opacity: 0.9; 
 border-radius:9px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='unselected'] {  
 width:15px; 
 height:15px; 
 background-color: #000000; 
 opacity: 0.5; 
 border-radius:7px; 
}
```
