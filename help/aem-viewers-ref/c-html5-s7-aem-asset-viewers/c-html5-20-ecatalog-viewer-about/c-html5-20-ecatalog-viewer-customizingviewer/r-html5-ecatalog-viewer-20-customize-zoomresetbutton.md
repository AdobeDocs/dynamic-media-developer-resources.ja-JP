---
description: このボタンをクリックまたはタップすると、メインビューの画像がリセットされます。 このボタンは、デスクトップシステムおよびタブレットのメインコントロールバーに表示されます。 携帯電話では、このボタンは画像の上の中央下に表示されます。 ただし、画像がリセット状態の場合は表示されません。 CSSを使用して、このボタンのサイズ設定、スキン表示、位置設定を行うことができます。
solution: Experience Manager
title: ズームリセットボタン
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog
role: Developer,User
exl-id: 6f0e22cd-12bd-4997-b874-539962504d3e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---

# ズームリセットボタン{#zoom-reset-button}

このボタンをクリックまたはタップすると、メインビューの画像がリセットされます。 このボタンは、デスクトップシステムおよびタブレットのメインコントロールバーに表示されます。 携帯電話では、このボタンは画像の上の中央下に表示されます。 ただし、画像がリセット状態の場合は表示されません。 CSSを使用して、このボタンのサイズ設定、スキン表示、位置設定を行うことができます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

ボタンの外観は、以下のCSSクラスセレクターを使用して制御します。

`.s7ecatalogviewer .s7zoomresetbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップおよびタブレットの場合）またはビューア（携帯電話の場合）の上の境界線からの位置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップおよびタブレットの場合）またはビューア（携帯電話の場合）の右の境界線からの位置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左 </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップおよびタブレットの場合）またはビューア（携帯電話の場合）の左の境界線からの位置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップおよびタブレットの場合）またはビューア（携帯電話の場合）の下の境界線からの位置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>ボタンの特定の状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合の、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSSスプライト</a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、 `state`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 — 28 x 28ピクセルで、（デスクトップ上に）メインコントロールバーの下から4ピクセルおよび右端から47ピクセルの位置に配置し、ボタンの4つの状態ごとに異なる画像を表示するズームリセットボタンを設定します。

```
.s7ecatalogviewer .s7zoomresetbutton { 
bottom:4px; 
right:47px; 
width:28px; 
height:28px; 
} 
.s7ecatalogviewer .s7zoomresetbutton [state='up'] { 
background-image:url(images/v2/ZoomResetButton_dark_up.png); 
} 
.s7ecatalogviewer .s7zoomresetbutton [state='over'] {  
background-image:url(images/v2/ZoomResettButton_dark_over.png); 
} 
.s7ecatalogviewer .s7zoomresetbutton [state='down'] {  
background-image:url(images/v2/ZoomResetButton_dark_down.png); 
} 
.s7ecatalogviewer .s7zoomresetbutton [state='disabled'] { 
background-image:url(images/v2/ZoomResetButton_dark_disabled.png); 
}
```
