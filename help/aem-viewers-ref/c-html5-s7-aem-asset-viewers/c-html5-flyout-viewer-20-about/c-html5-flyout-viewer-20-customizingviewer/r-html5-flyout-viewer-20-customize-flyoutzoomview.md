---
description: メインビューは、静的な画像、フライアウトビューで表示されるズームされた画像、静的な画像の上に表示されるハイライトのナビゲーション領域、静的な画像の上に表示されるチップメッセージで構成されます。
seo-description: メインビューは、静的な画像、フライアウトビューで表示されるズームされた画像、静的な画像の上に表示されるハイライトのナビゲーション領域、静的な画像の上に表示されるチップメッセージで構成されます。
seo-title: フライアウトズームビュー
solution: Experience Manager
title: フライアウトズームビュー
topic: Dynamic media
uuid: 35c60228-3044-442b-a8e2-e13d0bd306a5
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Flyout zoom view{#flyout-zoom-view}

メインビューは、静的な画像、フライアウトビューで表示されるズームされた画像、静的な画像の上に表示されるハイライトのナビゲーション領域、静的な画像の上に表示されるチップメッセージで構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

表示中の画像の寸法がフライアウトズームビューの寸法と一致しない場合、画像コンテンツはフライアウトズームビューの長方形の表示領域の中央に配置されます。

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

**フライアウトビューのCSSプロパティ**

フライアウトビューの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom
```

<table id="table_85446C72FD914594B7D108381BBFC673"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左 </span> </p> </td> 
   <td colname="col2"> <p> メインビューの左上隅を基準とした、フライアウトビューの水平方向の位置。 </p> </td> 
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
   <td colname="col2"> <p>フライアウトビューの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p>フライアウトビューの境界線。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 600 x 400ピクセルで、前の例に示した512 x 288のメインビューの右に100ピクセルのオフセットで表示するフライアウトビューを設定するには、次のように記述します。

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**メインビューでのハイライトのCSSプロパティ**

メインビューでのハイライトの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

CSSを使用して、背景、境界線、透明度および類似の属性を制御できます。 ただし、ハイライトのDOM要素のサイズと位置は、ビューアのロジックで管理されます。 CSSによる上書きはサポートされていません。

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> ハイライトのカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p> ハイライトの不透明度 </p> <p>Internet Explorer 8の場合は、 <span class="codeph"> filter:alpha(opacity-...) )；を使用します。 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p>境界線のハイライト。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 透明度が40 %で、赤い境界線が1ピクセルの緑色のハイライトを設定するには、次のように記述します。

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**カーソルのCSSプロパティ**

parameterをに設 `highlightmode` 定すると、メ `cursor`インビューのハイライトは固定サイズのカーソルアートワークに置き換えられ、これはCSSクラスセレクターを使用して制御します。

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

CSSを使用して、背景の画像とサイズを制御できます。

適用可能なCSSプロパティは次のとおりです。

<table id="table_A86F1E4DE9E84E11AF47373ADC63A459"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>カーソルのアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>カーソルの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>カーソルの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>カーソルは、属性セレ `input` クターをサポートします。このセレクターは、デバイスごとに異なるカーソルのアートワークとサイズを適用するのに使用できます。 特に、はデスクトップ `input="mouse"` システムに対応し、タッチデバ `input="touch"` イスに対応しています。

**オーバーレイのCSSプロパティ**

このパラメ `overlay` ーターをに設定す `1`ると、ハイライトフレームまたはカーソル画像の周囲の領域は、CSSクラスセレクターを使用して制御します。

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7overlay
```

<table id="table_A50CA8213C3A4682A081D3D30089574C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>オーバーレイのカラー </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p>オーバーレイの不透明度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**ヒントメッセージのCSSプロパティ**

ヒントメッセージの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

CSSを使用して、フォントスタイル、サイズの外観、垂直方向のオフセットを設定できます。 ただし、水平方向の位置揃えは、ビューアのロジックで管理されます。 またはプロパティを使用したCSS `left` からの `right` 上書きはサポートされていません。

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
   <td colname="col2"> <p>メインビューの下端からのオフセット。 </p> </td> 
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
   <td colname="col2"> <p>フォントサイズ </p> </td> 
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
   <td colname="col2"> <p>メッセージテキストの背景の不透明度。 </p> <p>Internet Explorer 8の場合は、 <span class="codeph"> filter:alpha(opacity-...) )を使用します。 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

ヒントメッセージはローカライズできます。 詳しくは、 [ユーザインターフェイス要素のローカリゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) を参照してください。

例 — 半透明のチップメッセージを、白のArial 12pxフォント、メインビューの下端から50ピクセルのオフセット、パディングおよび角丸の境界線で設定するには、次のように記述します。

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

