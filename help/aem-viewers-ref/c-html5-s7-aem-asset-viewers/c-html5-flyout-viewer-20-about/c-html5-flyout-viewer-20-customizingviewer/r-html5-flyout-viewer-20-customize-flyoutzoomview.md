---
title: フライアウトズームビュー
description: メインビューは、フライアウトビューに表示される静的な画像とズームされた画像で構成されます。 また、静的な画像の上に表示されるハイライトナビゲーション領域と、静的な画像の上に表示されるヒントメッセージで構成されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: c04c4b8f-4e63-4e84-98c0-aa0781608130
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 2%

---

# フライアウトズームビュー{#flyout-zoom-view}

メインビューは、フライアウトビューに表示される静的な画像とズームされた画像で構成されます。 また、静的な画像の上に表示されるハイライトナビゲーション領域と、静的な画像の上に表示されるヒントメッセージで構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

表示中の画像のサイズがフライアウトズーム表示のサイズと一致しない場合、画像コンテンツはフライアウトズーム表示の長方形表示領域内に中央揃えになります。

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

**フライアウトビューの CSS プロパティ**

フライアウトビューの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom
```

<table id="table_85446C72FD914594B7D108381BBFC673"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左 </span> </p> </td> 
   <td colname="col2"> <p> メインビューの左上隅を基準とした、フライアウトビューの水平位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p> メインビューの左上隅を基準とした、フライアウトビューの垂直方向の位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> フライアウトビューの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>フライアウトビューの高さです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p>フライアウトビューの境界線。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — フライアウトビューを 600 x 400 ピクセルに設定し、前の例に示した 512 x 288 のメインビューの右側に 100 ピクセルのオフセットで表示するには、次のように記述します。

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**メインビューでのハイライトの CSS プロパティ**

メインビューでのハイライトの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

CSS を使用して、背景、境界線、透明度および類似の属性を制御できます。 ただし、ハイライトの DOM 要素のサイズと位置は、ビューアのロジックによって管理されます。 CSS による上書きはサポートされていません。

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> ハイライトの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p> ハイライトの不透明度 </p> <p>Internet Explorer 8 の場合は、 <span class="codeph"> filter:alpha(opacity-...); </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p>境界線のハイライト。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 40%の透明度と 1 ピクセルの赤い境界線を持つ緑のハイライトを設定するには、次のように記述します。

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**カーソルの CSS プロパティ**

条件 `highlightmode` パラメーターが `cursor`、メインビュー内のハイライトは、固定サイズのカーソルアートワークに置き換えられます。このアートワークは、 CSS クラスセレクターで制御します。

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

CSS を使用して、背景画像とサイズを制御できます。

適用可能な CSS プロパティは次のとおりです。

<table id="table_A86F1E4DE9E84E11AF47373ADC63A459"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>カーソルのアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>カーソルの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>カーソルの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>カーソルは、 `input` 属性セレクター。デバイスごとに異なるカーソルのアートワークやサイズを適用するのに使用できます。 特に `input="mouse"` デスクトップシステムに対応し、 `input="touch"` は、タッチデバイスに対応します。

**オーバーレイの CSS プロパティ**

次の場合に `overlay` パラメーターが `1`に指定する場合、ハイライトフレームまたはカーソル画像の周囲の領域は、CSS クラスセレクターを使用して制御します。

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7overlay
```

<table id="table_A50CA8213C3A4682A081D3D30089574C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>オーバーレイの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p>オーバーレイの不透明度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

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

ヒントメッセージはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) を参照してください。

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
