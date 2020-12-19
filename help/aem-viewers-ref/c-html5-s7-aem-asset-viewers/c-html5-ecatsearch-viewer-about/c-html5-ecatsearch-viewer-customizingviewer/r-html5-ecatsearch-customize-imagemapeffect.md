---
description: modeパラメータの値に応じて、Viewerでは、マップが最初にScene7 Publishing Systemで作成された場所に、メイン表示の上に画像マップアイコンが表示されるか、元の画像マップの形状と一致する正確な領域がレンダリングされます。
seo-description: modeパラメータの値に応じて、Viewerでは、マップが最初にScene7 Publishing Systemで作成された場所に、メイン表示の上に画像マップアイコンが表示されるか、元の画像マップの形状と一致する正確な領域がレンダリングされます。
seo-title: 画像マップエフェクト
solution: Experience Manager
title: 画像マップエフェクト
topic: Dynamic media
uuid: 8bafaec3-500c-4a1f-b511-bff125daab7f
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 1%

---


# 画像マップエフェクト{#image-map-effect}

modeパラメータの値に応じて、Viewerでは、マップが最初にScene7 Publishing Systemで作成された場所に、メイン表示の上に画像マップアイコンが表示されるか、元の画像マップの形状と一致する正確な領域がレンダリングされます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

画像マップアイコンの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>以前の画像マップアイコンのスタイル設定に使用された`s7mapoverlay` CSSクラスは非推奨になりました。代わりに`s7icon`を使用します。

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>画像マップアイコンのアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSSスプライト</a>も参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>画像マップアイコンの幅（ピクセル単位） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>画像マップアイコンの高さ（ピクセル単位） </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>画像マップアイコンでは、`state`属性セレクターがサポートされます。このセレクターは、アイコンの状態`default`と`active`に異なるスキンを適用するのに使用できます。

例 — 28 x 28ピクセルで、2つのアイコンの状態ごとに異なる画像を表示する画像マップアイコンを設定します。

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

[画像マップのサポート](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a)も参照してください。

画像マップ領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region
```

<table id="table_1FF98CE842604AAABD838FF528CDC4EF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background  </span> </p> </td> 
   <td colname="col2"> <p> 画像マップ領域の塗りのカラー </p> <p>#RRGGBB、RGB(R,G,B)またはRGBA(R,G,B,A)形式で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 画像マップ領域の塗りのカラー </p> <p>#RRGGBB、RGB(R,G,B)またはRGBA(R,G,B,A)形式で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p> 画像マップ領域の境界線のスタイル </p> <p><span class="codeph"> <span class="varname">幅</span>べた塗りの<span class="varname">色</span> </span>として指定します。<span class="codeph"> <span class="varname">幅</span> </span>はピクセル単位で表し、<span class="codeph"> <span class="varname">色</span>は設定します。#RRGGBB、RGB(R,G,B)またはRGBA(R,G,B,A)です。</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — `1`ピクセルの黒い境界線を持つ透明な画像マップ領域を設定します。

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

