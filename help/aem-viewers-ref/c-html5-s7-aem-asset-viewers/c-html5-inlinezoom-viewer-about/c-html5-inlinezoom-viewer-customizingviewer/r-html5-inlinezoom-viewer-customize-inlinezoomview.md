---
description: メインビューは、静的な画像、フライアウトビューの静的な画像の上に表示されるズームされた画像、静的な画像の上に表示されるチップメッセージで構成されます。
solution: Experience Manager
title: フライアウトズームビュー
feature: Dynamic Media Classic，ビューア，SDK/API，インラインズーム
role: Developer,User
exl-id: 7b4b5cc9-68ad-4e7a-a2d9-3bbced929145
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 1%

---

# フライアウトズームビュー{#flyout-zoom-view}

メインビューは、静的な画像、フライアウトビューの静的な画像の上に表示されるズームされた画像、静的な画像の上に表示されるチップメッセージで構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューのCSSプロパティ**

メインビューの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7flyoutviewer .s7flyoutzoomview
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

**チップメッセージのCSSプロパティ**

ヒントメッセージの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

CSSを使用して、フォントスタイル、サイズの外観、垂直方向のオフセットを設定できます。 ただし、水平方向の整列はビューアのロジックで管理されます。 `left`または`right`プロパティを使用したCSSによる上書きはサポートされていません。

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
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
   <td colname="col2"> <p>テキストカラー </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>フォント名 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>メッセージテキストの周囲のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>メッセージテキストの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p>メッセージテキストの背景の境界線の半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明  </span> </p> </td> 
   <td colname="col2"> <p>メッセージテキストの背景の不透明度。 </p> <p>Internet Explorer 8の場合は、 <span class="codeph"> filter:alpha(opacity-...) ) </span>を使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ヒントメッセージはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27)を参照してください。

.

例 — 半透明のチップメッセージを、白のArial 12pxフォント、メインビューの下端から50ピクセルのオフセット、パディング、丸めた境界線付きで設定するには、次のように記述します。

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
