---
title: フライアウトズームビュー
description: メインビューは、静的画像と、静的画像の上にあるフライアウトビューに表示されるズームされた画像で構成されます。 また、静的な画像の上に表示されるヒントメッセージで構成されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 7b4b5cc9-68ad-4e7a-a2d9-3bbced929145
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 1%

---

# フライアウトズームビュー{#flyout-zoom-view}

メインビューは、静的画像と、静的画像の上にあるフライアウトビューに表示されるズームされた画像で構成されます。 また、静的な画像の上に表示されるヒントメッセージで構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューの CSS プロパティ**

メインビューの外観は、以下の CSS クラスセレクターを使用して制御します。

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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> メインビューの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — メインビューを透明にするには、次のように記述します。

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**ヒントメッセージの CSS プロパティ**

ヒントメッセージの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

CSS を使用して、フォントスタイル、サイズ、外観、垂直方向のオフセットを設定できます。 ただし、水平方向の位置揃えはビューアのロジックで管理します。 を使用した CSS による上書き `left` または `right` プロパティはサポートされていません。

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
   <td colname="col2"> <p>メインビューの下部からのオフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>テキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>フォント名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>メッセージテキストの周囲のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>メッセージテキストの背景の塗りのカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>メッセージテキストの背景の境界線の半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p>メッセージテキストの背景の不透明度。 </p> <p>Internet Explorer 8 の場合は、 <span class="codeph"> filter:alpha(opacity-...) ) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

ヒントメッセージはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) を参照してください。

.

例 — 半透明のチップメッセージを、白い Arial® 12-px フォント、メインビューの下から 50 ピクセルのオフセット、パディング、丸めた境界線付きで設定するには、次のように記述します。

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
