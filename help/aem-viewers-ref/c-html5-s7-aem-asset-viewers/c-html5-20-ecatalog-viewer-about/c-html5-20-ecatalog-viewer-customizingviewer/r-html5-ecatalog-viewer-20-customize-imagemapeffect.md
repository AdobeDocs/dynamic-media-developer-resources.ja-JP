---
title: 画像マップエフェクト
description: mode パラメーターの値に応じて、ビューアは画像マップアイコンをDynamic Media Classicでマップが最初に作成された場所のメインビューに表示します。 または、元の画像マップの形状に一致する正確な領域をレンダリングします。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3816118f-4eb7-4436-9f54-155dde077734
source-git-commit: 6087b48b898e93e605c3873cbd5132b74d04225f
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---

# 画像マップエフェクト{#image-map-effect}

mode パラメーターの値に応じて、ビューアは画像マップアイコンをDynamic Media Classicでマップが最初に作成された場所のメインビューに表示します。 または、元の画像マップの形状に一致する正確な領域をレンダリングします。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域の CSS プロパティ**

画像マップアイコンの外観は、次の CSS クラスセレクターで制御します。

```
.s7ecatalogviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>過去に画像マップアイコンのスタイル設定に使用されていた `s7mapoverlay` CSS クラスは非推奨（廃止予定）になりました。代わりに `s7icon` を使用します。

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>画像マップ アイコン アートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> ール </a> 参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>画像マップアイコンの幅（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>画像マップアイコンの高さ（ピクセル単位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>画像マップアイコンは、`state` 属性セレクターをサポートしています。このセレクターを使用して、`default` と `active` のアイコン状態に異なるスキンを適用できます。

例 – 28 x 28 ピクセルの画像マップアイコンを設定します。このアイコンは、2 つの異なるアイコン状態のそれぞれに異なる画像を表示します。

```
.s7ecatalogviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

[ 画像マップのサポート ](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a) も参照してください。

画像マップ領域の外観は、次の CSS クラスセレクターで制御します。

```
.s7ecatalogviewer .s7imagemapeffect .s7region
```

<table id="table_1FF98CE842604AAABD838FF528CDC4EF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background </span> </p> </td> 
   <td colname="col2"> <p> 画像マップ領域の塗りつぶしの色。 </p> <p>#RRGGBB、RGB（R,G,B）または RGBA （R,G,B,A）形式で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p> 画像マップ領域の塗りつぶしの色。 </p> <p>#RRGGBB、RGB（R,G,B）または RGBA （R,G,B,A）形式で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 境界線 </span> </p> </td> 
   <td colname="col2"> <p> 画像マップ領域の境界線のスタイル。 </p> <p><span class="codeph"> <span class="varname"> 幅 </span> 単色 <span class="varname"> 色 </span></span> と指定します。<span class="codeph"> <span class="varname"> 幅 </span></span> はピクセル単位で表され、<span class="codeph"> <span class="varname"> 色 </span></span> は#RRGGBB、RGB（R,G,B）または RGBA （R,G,B,A）に設定されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – ピクセルの黒い境界線を持つ透明画像マップ領域 `1` 設定する

```
.s7ecatalogviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
