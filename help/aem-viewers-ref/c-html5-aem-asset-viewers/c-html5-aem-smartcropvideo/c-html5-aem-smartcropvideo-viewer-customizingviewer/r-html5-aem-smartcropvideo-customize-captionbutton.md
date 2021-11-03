---
title: キャプションボタン
description: クローズドキャプションの表示/非表示を切り替えます。 キャプションパラメーターが指定されていない場合は表示されません。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 47d4a33b-e2bc-4a32-be45-5320d3de1955
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 2%

---

# キャプションボタン{#caption-button}

クローズドキャプションの表示/非表示を切り替えます。 キャプションパラメーターが指定されていない場合は表示されません。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

CSS を使用して、このボタンのサイズ、スキン、およびこのボタンを含むコントロールバーに対する位置を設定できます。

このボタンの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7closedcaptionbutton
```

**キャプションボタンの CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p> パディングを含む上の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p> パディングを含む右の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左 </span> </p> </td> 
   <td colname="col2"> <p> パディングを含む左の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>パディングを含む下の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> フルスクリーンボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>フルスクリーンボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>詳しくは、 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、 `state` および `selected` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。 特に `selected='true'` は、キャプションが表示されている状態と、 `selected='false'` は、キャプションが非表示の場合に使用されます。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

28 x 28 ピクセルのクローズドキャプションボタンを設定するには、次のように記述します。 コントロールバーの上から 4 ピクセル、右端から 68 ピクセルの位置に配置されます。 最後に、は、選択時または未選択時の 4 つの異なるボタン状態ごとに異なる画像を表示します。

```
.s7smartcropvideoviewer .s7closedcaptionbutton { 
 position:absolute; 
 top:4px; 
 right:68px; 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7closedcaptionbutton[selected='true'][state='up'] { 
background-image:url(images/v2/ClosedCaptionButton_up.png); 
} 
.s7smartcropvideoviewer .s7closedcaptionbutton[selected='true'][state='over'] { 
background-image:url(images/v2/ClosedCaptionButton_over.png); 
} 
.s7smartcropvideoviewer .s7closedcaptionbutton[selected='true'][state='down'] { 
background-image:url(images/v2/ClosedCaptionButton_down.png); 
} 
.s7smartcropvideoviewer .s7closedcaptionbutton[selected='true'][state='disabled'] { 
background-image:url(images/v2/ClosedCaptionButton_disabled.png); 
} 
.s7smartcropvideoviewer .s7closedcaptionbutton[selected='false'][state='up'] { 
background-image:url(images/v2/ClosedCaptionButton_disabled.png); 
} 
.s7smartcropvideoviewer .s7closedcaptionbutton[selected='false'][state='over'] { 
background-image:url(images/v2/ClosedCaptionButton_over.png); 
} 
.s7smartcropvideoviewer .s7closedcaptionbutton[selected='false'][state='down'] { 
background-image:url(images/v2/ClosedCaptionButton_down.png); 
} 
.s7smartcropvideoviewer .s7closedcaptionbutton[selected='false'][state='disabled'] { 
background-image:url(images/v2/ClosedCaptionButton_disabled.png);  
}
```
