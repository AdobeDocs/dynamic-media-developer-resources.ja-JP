---
description: 設定インジケーターは、ビューアの下部にレンダリングされる一連のドットです。 セット内の現在位置を表示します。
seo-description: 設定インジケーターは、ビューアの下部にレンダリングされる一連のドットです。 セット内の現在位置を表示します。
seo-title: 設定インジケーター
solution: Experience Manager
title: 設定インジケーター
topic: Dynamic media
uuid: 3f90a216-654f-44a9-947d-592bd5f342d4
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 1%

---


# インジケータを設定{#set-indicator}

設定インジケーターは、ビューアの下部にレンダリングされる一連のドットです。 セット内の現在位置を表示します。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**設定インジケーターのCSSプロパティ**

設定インジケーターコンテナの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7carouselviewer .s7setindicator
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
   <td colname="col2"> <p>設定インジケーターの16進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>設定インジケーターでは、mode属性セレクターがサポートされます。このセレクターは、点線と数値の操作モードに対して異なるスタイルを適用するのに使用できます。 特に、`mode="numeric"`は数値演算モードに対応します。`mode="dotted"`は、デフォルトのドットの状態に対応します。

例 — 白の背景でインジケーターを設定するには、次のように記述します。

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

個々の設定インジケーターのドットの外観は、CSSクラスセレクターを使用して制御します。 これは、点線と数値の両方の操作モードの項目に適用されます。

`.s7carouselviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
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
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p>左余白（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p>上余白（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right  </span> </p> </td> 
   <td colname="col2"> <p>右マージン（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-bottom  </span> </p> </td> 
   <td colname="col2"> <p>下余白（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p>境界線の半径（ピクセル単位） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>16進数形式の背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>フォントの名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>フォントのサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>フォントの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertical-align  </span> </p> </td> 
   <td colname="col2"> <p>バナーのインデックスの垂直方向の配置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height  </span> </p> </td> 
   <td colname="col2"> <p>バナーインデックスのテキストの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>設定インジケーター項目では、`state`属性セレクターがサポートされます。このセレクターは、サムネールの状態ごとに異なるスキンを適用するのに使用できます。 特に、`state="selected"`はセット内の現在の要素に対応します。`state="unselected"`は、デフォルトの項目状態に対応します。

例 — デスクトップシステムをビューアの下端から20ピクセルの位置に配置するための設定インジケーターを点線モードで設定するには、次のように記述します。 選択されていないドットは、50 %の透明度を持つ黒で表示されます。15 x 15ピクセルの角が7ピクセルの場合、 選択したドットは、90 %の透明度を持つ黒、18 x 18ピクセルの角を9ピクセル丸めた黒です。 ドット間の間隔は5ピクセルです。

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

