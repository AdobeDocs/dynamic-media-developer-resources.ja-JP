---
title: フライアウトズーム表示
description: メインビューは、静止画像と、静止画像の上のフライアウトビューに表示されるズームされた画像で構成されます。 また、静止画像の上に表示されるチップメッセージで構成されています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 7b4b5cc9-68ad-4e7a-a2d9-3bbced929145
TQID: 'https://experienceleague.adobe.com/Ahaz6TsxhAqEHsIe961PjJKLta7Bfv0sWvdioSO849g'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 272
ht-degree: 0%

---

# フライアウトズーム表示{#flyout-zoom-view}

メインビューは、静止画像と、静止画像の上のフライアウトビューに表示されるズームされた画像で構成されます。 また、静止画像の上に表示されるチップメッセージで構成されています。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

メインビューの&#x200B;**CSS プロパティ**

メインビューの外観は、次のCSS クラスセレクターで制御されます。

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
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
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

ヒント メッセージの&#x200B;**CSS プロパティ**

チップメッセージの外観は、次のCSS クラスセレクターで制御されます。

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

CSSを使用して、フォントスタイル、サイズ、アピアランス、および垂直オフセットを設定できます。 ただし、水平方向の整列はビューアロジックによって管理されます。 `left`または`right` プロパティを使用したCSSによる上書きはサポートされていません。

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">下</span> </p> </td> 
   <td colname="col2"> <p>メインビューの下部からオフセットします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p>テキストの色： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>フォント名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>メッセージテキストの周囲のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>メッセージテキストの背景色の塗りつぶし。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>メッセージテキストの背景境界線の半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">不透明度</span> </p> </td> 
   <td colname="col2"> <p>メッセージテキストの背景の不透明度 </p> <p>Internet Explorer 8の場合、<span class="codeph"> filter:alpha （opacity-...）） </span>を使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ヒント メッセージはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27)を参照してください。

.

例 – 白いArial® 12 px フォント、メインビューの下部から50 ピクセルのオフセット、パディング、丸みを帯びた境界線を使用して、半透明のチップ メッセージを設定するには：

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
