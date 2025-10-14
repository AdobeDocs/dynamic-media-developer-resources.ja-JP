---
title: フライアウトズームビュー
description: メインビューは、静的な画像と、静的な画像の上のフライアウトビューに表示されるズームされた画像で構成されます。 また、静的画像の上に表示される先端メッセージでも構成されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 7b4b5cc9-68ad-4e7a-a2d9-3bbced929145
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# フライアウトズームビュー{#flyout-zoom-view}

メインビューは、静的な画像と、静的な画像の上のフライアウトビューに表示されるズームされた画像で構成されます。 また、静的画像の上に表示される先端メッセージでも構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューの CSS プロパティ**

メインビューの外観は、次の CSS クラスセレクターで制御します。

```
.s7flyoutviewer .s7flyoutzoomview
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
   <td colname="col2"> <p> メインビューの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – メインビューを透明にするには：

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**Tip メッセージの CSS プロパティ**

先端メッセージの外観は、次の CSS クラスセレクターで制御します。

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

CSS を使用すると、フォントスタイル、サイズ、外観、垂直オフセットを設定できます。 ただし、水平方向の整列はビューアのロジックで管理されます。 `left` または `right` プロパティを使用した CSS による上書きはサポートされていません。

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>メイン ビューの下部からのオフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>テキストのカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>フォント名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>メッセージテキストの周囲のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>メッセージテキストの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>メッセージテキストの背景色の半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacity </span> </p> </td> 
   <td colname="col2"> <p>メッセージテキストの背景の不透明度。 </p> <p>Internet Explorer 8 の場合は、filter:alpha （opacity-...） <span class="codeph"> を使用 </span> ます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ヒント メッセージはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) を参照してください。

.

例 – 白い Arial® 12 ピクセルのフォント、メインビューの下部からの 50 ピクセルのオフセット、パディング、丸い境界線を使用して、半透明の先端メッセージを設定するには：

```
.s7flyoutviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```
