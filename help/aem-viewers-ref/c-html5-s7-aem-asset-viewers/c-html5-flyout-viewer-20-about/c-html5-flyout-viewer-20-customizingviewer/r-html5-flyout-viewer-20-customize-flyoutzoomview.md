---
title: フライアウトズームビュー
description: メインビューは、静的な画像と、フライアウトビューに表示されるズームされた画像で構成されます。 また、静的画像上に表示されるハイライトナビゲーション領域と、静的画像上に表示されるヒントメッセージも含まれます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: c04c4b8f-4e63-4e84-98c0-aa0781608130
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# フライアウトズームビュー{#flyout-zoom-view}

メインビューは、静的な画像と、フライアウトビューに表示されるズームされた画像で構成されます。 また、静的画像上に表示されるハイライトナビゲーション領域と、静的画像上に表示されるヒントメッセージも含まれます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

表示されている画像の寸法がフライアウトズームビューの寸法と一致しない場合、画像コンテンツはフライアウトズームビューの長方形表示領域の中央に配置されます。

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

**フライアウトビューの CSS プロパティ**

フライアウト表示の外観は、次の CSS クラスセレクターで制御します。

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
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p> フライアウトビューの水平位置。メイン ビューの左上コーナーを基準にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 天 </span> </p> </td> 
   <td colname="col2"> <p> メイン ビューの左上コーナーを基準にした、フライアウト ビューの垂直位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p> フライアウトビューの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>フライアウトビューの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 境界線 </span> </p> </td> 
   <td colname="col2"> <p>フライアウト ビューの境界です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 前述の例に示すように、フライアウト表示を 600 x 400 ピクセルに設定し、512 x 288 のメイン表示の右側に 100 ピクセルのオフセットで表示するには、次のようにします。

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**メインビューのハイライト表示の CSS プロパティ**

メインビューでのハイライトの外観は、次の CSS クラスセレクターで制御します。

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

CSS を使用して、背景、境界線、透明度などの属性を制御できます。 ただし、ハイライト表示の DOM 要素のサイズと位置は、ビューアのロジックによって管理されます。 CSS による上書きはサポートされていません。

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p> ハイライトの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacity </span> </p> </td> 
   <td colname="col2"> <p> ハイライトの不透明度。 </p> <p>Internet Explorer 8 の場合、<span class="codeph"> filter:alpha （opacity-...））; </span> を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 境界線 </span> </p> </td> 
   <td colname="col2"> <p>境界線がハイライト表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 40% の透明度と 1 ピクセルの赤い境界線を持つ緑のハイライトを設定するには：

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**カーソルの CSS プロパティ**

パラメーター `highlightmode` `cursor` に設定すると、メインビューのハイライト表示は固定サイズのカーソルアートワークに置き換えられ、CSS クラスセレクターで制御されます。

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

CSS を使用して背景画像とサイズを制御することができます。

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
   <td colname="col2"> <p>カーソルアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>カーソルの幅 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>カーソルの高さ </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>カーソルは `input` 属性セレクターをサポートしており、異なるデバイスに異なるカーソルアートワークとサイズを適用するために使用できます。 特に、`input="mouse"` はデスクトップシステムに対応し、`input="touch"` はタッチデバイスに対応しています。

**オーバーレイの CSS プロパティ**

`overlay` パラメーターを `1` に設定すると、ハイライトフレームまたはカーソル画像の周囲の領域が、CSS クラスセレクターで制御されます。

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
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>オーバーレイカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacity </span> </p> </td> 
   <td colname="col2"> <p>オーバーレイの不透明度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

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
   <td colname="col2"> <p>メッセージテキストの背景の不透明度。 </p> <p>Internet Explorer 8 の場合は、filter:alpha （opacity-...） </span> を使用 <span class="codeph"> ます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ヒント メッセージはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) を参照してください。

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
