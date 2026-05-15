---
title: インジケーターを設定
description: Set インジケーターは、ビューアの下部に表示される一連のドットです。 セット内の現在の位置が表示されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 7d0827c5-f420-4804-983c-5298ee92b276
TQID: 'https://experienceleague.adobe.com/VF5K2OQes7ej6M1YGwefbZ4LLnsHVuXed0MKXoX79u0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 354
ht-degree: 0%

---

# インジケーターを設定{#set-indicator}

Set インジケーターは、ビューアの下部に表示される一連のドットです。 セット内の現在の位置が表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

セット インジケーターの&#x200B;**CSS プロパティ**

Set インジケーターコンテナの外観は、次のCSS クラスセレクターで制御されます。

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
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>セットインジケーターの16進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Set インジケーターは、モード属性セレクターをサポートしています。このセレクターを使用すると、点線と数値の操作モードに様々なスタイルを適用できます。 特に、`mode="numeric"`は数値演算モードに対応し、`mode="dotted"`はデフォルトのドット状態に対応します。

例えば、白い背景の設定インジケーターを設定するとします。

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

個々のセットインジケーターのドットの外観は、CSS クラスセレクターで制御されます。 点線モードと数値演算モードの両方の項目に適用されます。

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
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>セットインジケーターのドットの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>セットインジケーターのドットの高さ。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph">右余白</span> </p> </td> 
   <td colname="col2"> <p>右マージン（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-bottom </span> </p> </td> 
   <td colname="col2"> <p>下余白（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>境界線の半径（ピクセル単位） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>16進数形式の背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>フォント名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>フォントのサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p>フォントの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">垂直整列</span> </p> </td> 
   <td colname="col2"> <p>バナーインデックスの垂直方向の整列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">行の高さ</span> </p> </td> 
   <td colname="col2"> <p>バナーインデックスのテキスト高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>インジケーター項目を設定すると、`state`属性セレクターがサポートされます。このセレクターを使用すると、異なるサムネール状態に異なるスキンを適用できます。 特に、`state="selected"`はセット内の現在の要素に対応し、`state="unselected"`はデフォルトの項目状態に対応します。

例えば、デスクトップシステムのセットインジケーターを点線モードで設定するとします。 ビューアの下部から20 ピクセルの位置に配置します。 また、選択していないドットは透明50%、15 x 15 ピクセル、角を丸めた7 ピクセルの黒にすることができます。 選択したドットは黒で、透明度は90%、18 x 18 ピクセル、角は9 ピクセルです。 ドット間の間隔は5 ピクセルです。

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
