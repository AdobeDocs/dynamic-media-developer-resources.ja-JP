---
description: メイン表示は、静的な画像、フライアウト表示で静的な画像の上に表示されるズームされた画像、静的な画像の上に表示されるチップメッセージで構成されます。
seo-description: メイン表示は、静的な画像、フライアウト表示で静的な画像の上に表示されるズームされた画像、静的な画像の上に表示されるチップメッセージで構成されます。
seo-title: フライアウトズーム表示
solution: Experience Manager
title: フライアウトズーム表示
topic: Dynamic media
uuid: a918c775-a36a-44e8-9ca4-90cb8f5c3a5e
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 1%

---


# フライアウトズーム表示{#flyout-zoom-view}

メイン表示は、静的な画像、フライアウト表示で静的な画像の上に表示されるズームされた画像、静的な画像の上に表示されるチップメッセージで構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メイン表示のCSSプロパティ**

メイン表示の外観は、以下のCSSクラスセレクターを使用して制御します。

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
   <td colname="col2"> <p> メイン表示の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — メイン表示を透明にするには、次のように記述します。

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**チップメッセージのCSSプロパティ**

チップメッセージの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

フォントスタイル、サイズの外観、および垂直方向のオフセットは、CSSで設定できます。 ただし、水平方向の位置揃えはビューアのロジックに管理されます。 `left`プロパティまたは`right`プロパティを使用したCSSからの上書きはサポートされていません。

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
   <td colname="col2"> <p>メイン表示の下端からのオフセット。 </p> </td> 
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
   <td colname="col2"> <p>メッセージテキストの背景の塗りのカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p>メッセージテキストの背景の境界線の半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacity  </span> </p> </td> 
   <td colname="col2"> <p>メッセージテキストの背景の不透明度。 </p> <p>Internet Explorer 8の場合は、<span class="codeph"> filter:alpha(opacity-...) ) </span>を使用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ヒントメッセージはローカライズできます。 詳しくは、[ユーザインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27)を参照してください。

.

例 — 半透明のチップメッセージを、白のArial 12pxフォント、メイン表示の下端から50ピクセルのオフセット、パディングおよび角丸付きの境界線付きで設定するには、次のように記述します。

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

