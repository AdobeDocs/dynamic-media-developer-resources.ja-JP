---
title: 「キャプション」ボタン
description: このボタンは、クローズドキャプション表示のオンとオフを切り替えます。 キャプションパラメーターが指定されていない場合は表示されません。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 86b610e9-fea2-45b3-9b74-7ddd558fc267
TQID: 'https://experienceleague.adobe.com/UhXFpRntG1CZk9rv99ytbUrXV1OQP1RKB2C7r3M-YNo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 259
ht-degree: 0%

---

# 「キャプション」ボタン{#caption-button}

このボタンは、クローズドキャプション表示のオンとオフを切り替えます。 キャプションパラメーターが指定されていない場合は表示されません。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

CSSを使用して、このボタンを含むコントロールバーに対して、このボタンのサイズ、スキン、位置を調整できます。

このボタンの外観は、次のCSS クラスセレクターで制御されます。

```
.s7smartcropvideoviewer .s7closedcaptionbutton
```

キャプション ボタンの&#x200B;**CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上位</span> </p> </td> 
   <td colname="col2"> <p> パディングを含む上部境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p> パディングを含む右端からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">さんが</span>を残しました </p> </td> 
   <td colname="col2"> <p> パディングを含む左端からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">下</span> </p> </td> 
   <td colname="col2"> <p>パディングを含む下部境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p> フルスクリーンボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>フルスクリーンボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p> 特定のボタン状態の表示画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`と`selected`の両方の属性セレクターをサポートしており、異なるスキンを異なるボタンの状態に適用するために使用できます。 特に、`selected='true'`はキャプションが表示されている状態に対応し、`selected='false'`はキャプションが非表示の状態に使用されます。

ボタンツールのヒントはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)を参照してください。

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

28 x 28 ピクセルのクローズドキャプションボタンを設定するには、次の手順を実行します。 コントロールバーの上部から4 ピクセル、右端から68 ピクセルに配置されます。 最後に、選択または選択されていない4つの異なるボタンの状態ごとに異なる画像が表示されます。

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
