---
title: フライアウトズーム表示
description: メインビューは、フライアウトビューに表示される静止画像とズームされた画像で構成されます。 また、静止画像の上に表示されるハイライトナビゲーション領域と、静止画像の上に表示されるヒントのメッセージで構成されています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: c04c4b8f-4e63-4e84-98c0-aa0781608130
TQID: 'https://experienceleague.adobe.com/nQGoCR2S4Qo7lZnvRnzcYhnTWgGZYfYOHfXo1b1kYvE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 655
ht-degree: 0%

---

# フライアウトズーム表示{#flyout-zoom-view}

メインビューは、フライアウトビューに表示される静止画像とズームされた画像で構成されます。 また、静止画像の上に表示されるハイライトナビゲーション領域と、静止画像の上に表示されるヒントのメッセージで構成されています。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

表示される画像のサイズがフライアウトズームビューのサイズと一致しない場合、画像コンテンツはフライアウトズームビューの長方形表示領域内に中央に配置されます。

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

**フライアウトビューのCSS プロパティ**

フライアウトビューの外観は、次のCSS クラスセレクターで制御されます。

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
   <td colname="col1"> <p> <span class="codeph">さんが</span>を残しました </p> </td> 
   <td colname="col2"> <p> メインビューの左上隅に対するフライアウトビューの水平方向の位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上位</span> </p> </td> 
   <td colname="col2"> <p> メインビューの左上隅を基準とした、フライアウトビューの垂直位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p> フライアウトビューの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>フライアウトビューの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">境界線</span> </p> </td> 
   <td colname="col2"> <p>フライアウトビューの境界線。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 前の例で示した512 x 288のメインビューの右側に100 ピクセルがオフセットされたフライアウトビューを600 x 400 ピクセルに設定するには：

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

メインビューのハイライトの&#x200B;**CSS プロパティ**

メインビューでのハイライトの表示は、次のCSS クラスセレクターで制御されます。

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

CSSを使用して、背景、境界線、透明度などの属性を制御できます。 ただし、ハイライト DOM要素のサイズと位置は、ビューアロジックによって管理されます。 CSSによる上書きはサポートされていません。

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> ハイライトの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">不透明度</span> </p> </td> 
   <td colname="col2"> <p> 不透明度をハイライトします。 </p> <p>Internet Explorer 8の場合、<span class="codeph"> filter:alpha （opacity-...））; </span>を使用します </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">境界線</span> </p> </td> 
   <td colname="col2"> <p>境界線がハイライト表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 40%の透明度と1 ピクセルの赤い境界線で緑色のハイライトを設定するには：

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

カーソルの&#x200B;**CSS プロパティ**

`highlightmode` パラメーターが`cursor`に設定されている場合、メインビューのハイライトは、CSS クラスセレクターで制御される固定サイズのカーソルアートワークに置き換えられます。

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

CSSを使用して背景画像とサイズを制御することができます。

適用できるCSS プロパティは次のとおりです。

<table id="table_A86F1E4DE9E84E11AF47373ADC63A459"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p>カーソルのアートワーク： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>カーソルの幅： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>カーソルの高さ： </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Cursorは`input`属性セレクターをサポートしています。このセレクターを使用すると、異なるデバイスに対して異なるカーソルアートワークとサイズを適用できます。 特に、`input="mouse"`はデスクトップシステムに対応し、`input="touch"`はタッチデバイスに対応します。

オーバーレイの&#x200B;**CSS プロパティ**

`overlay` パラメーターが`1`に設定されている場合、ハイライトフレームまたはカーソル画像の周囲の領域は、CSS クラスセレクターで制御されます。

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
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>オーバーレイカラー： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">不透明度</span> </p> </td> 
   <td colname="col2"> <p>オーバーレイの不透明度： </p> </td> 
  </tr> 
 </tbody> 
</table>

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

ヒント メッセージはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27)を参照してください。

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
