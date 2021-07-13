---
description: modeパラメータの値に応じて、ビューアは、Dynamic Media Classicでマップが最初に作成された場所にメインビューの上に画像マップアイコンを表示するか、元の画像マップの形状に一致する正確な領域をレンダリングします。
solution: Experience Manager
title: 画像マップエフェクト
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog
role: Developer,User
exl-id: 3816118f-4eb7-4436-9f54-155dde077734
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 1%

---

# 画像マップエフェクト{#image-map-effect}

modeパラメータの値に応じて、ビューアは、Dynamic Media Classicでマップが最初に作成された場所にメインビューの上に画像マップアイコンを表示するか、元の画像マップの形状に一致する正確な領域をレンダリングします。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

画像マップアイコンの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>以前の画像マップアイコンのスタイル設定に使用されていた`s7mapoverlay` CSSクラスは非推奨（廃止予定）となりました。代わりに、 `s7icon`を使用します。

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
   <td colname="col2"> <p> CSSスプライトを使用する場合の、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSSスプライト</a>も参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>画像マップアイコンの幅（ピクセル単位） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>画像マップアイコンの高さ（ピクセル単位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>画像マップアイコンでは、 `state`属性セレクターがサポートされます。このセレクターを使用して、アイコンの状態（`default`と`active`）に異なるスキンを適用できます。

例 — 28 x 28ピクセルで、2つの異なるアイコン状態ごとに異なる画像を表示する画像マップアイコンを設定します。

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

[画像マップのサポート](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a)も参照してください。

画像マップ領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7imagemapeffect .s7region
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
   <td colname="col1"> <p> <span class="codeph"> 背景  </span> </p> </td> 
   <td colname="col2"> <p> 画像マップ領域の塗りのカラー </p> <p>#RRGGBB、RGB(R,G,B)、またはRGBA(R,G,B,A)形式で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 画像マップ領域の塗りのカラー </p> <p>#RRGGBB、RGB(R,G,B)またはRGBA(R,G,B,A)形式で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p> 画像マップ領域の境界線のスタイル。 </p> <p><span class="codeph"> <span class="varname">幅</span>べた塗り<span class="varname">色</span> </span>で指定します。ここで、<span class="codeph"> <span class="varname">幅</span> </span>はピクセル単位、<span class="codeph"> <span class="varname">色</span> </span>は設定します。#RRGGBB, RGB(R,G,B)またはRGBA(R,G,B,A)。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — `1`ピクセルの黒い境界線を持つ透明な画像マップ領域を設定します。

```
.s7ecatalogviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
