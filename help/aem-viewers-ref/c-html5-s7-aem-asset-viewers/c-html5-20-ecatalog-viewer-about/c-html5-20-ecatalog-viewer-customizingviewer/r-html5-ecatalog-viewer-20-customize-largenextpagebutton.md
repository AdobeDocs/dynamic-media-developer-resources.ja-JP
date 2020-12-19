---
description: このボタンをクリックまたはタップすると、カタログの次のページに移動します。 このボタンは、メインコントロールバーに表示されます。 携帯電話では、画面サイズの制限を守るため、このボタンは表示されません。 このボタンのサイズ設定、スキン表示および配置は、CSSを使用して行うことができます。
seo-description: このボタンをクリックまたはタップすると、カタログの次のページに移動します。 このボタンは、メインコントロールバーに表示されます。 携帯電話では、画面サイズの制限を守るため、このボタンは表示されません。 このボタンのサイズ設定、スキン表示および配置は、CSSを使用して行うことができます。
seo-title: 次の大きいページボタン
solution: Experience Manager
title: 次の大きいページボタン
topic: Dynamic media
uuid: c10edce3-ea01-4c8b-bb43-c2aafed08a39
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 2%

---


# 次の大きいページボタン{#large-next-page-button}

このボタンをクリックまたはタップすると、カタログの次のページに移動します。 このボタンは、メインコントロールバーに表示されます。 携帯電話では、画面サイズの制限を守るため、このボタンは表示されません。 このボタンのサイズ設定、スキン表示および配置は、CSSを使用して行うことができます。

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**メインビューア領域のCSSプロパティ**

ボタンの外観は、以下のCSSクラスセレクターを使用して制御します。

`.s7ecatalogviewer .s7ecatrightbutton .s7panrightbutton`

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
   <td colname="col2"> <p>メインコントロールバーの上の境界線からの位置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバーの右の境界線からの位置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左 </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバーの左の境界線からの位置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバーの下の境界線からの位置（パディングを含む）。 </p> </td> 
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
   <td colname="col2"> <p>ボタンの特定の状態に対して表示する画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSSスプライト</a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、`state`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。

ボタンのツールチップをローカライズできます。 詳しくは、[ユーザインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 — 56 x 56ピクセルで、垂直方向に中央揃えしてビューアの右の境界線にアンカーし、ボタンの4つの状態ごとに異なる画像を表示する次の大きいページボタンを設定します。

```
.s7ecatalogviewer .s7ecatrightbutton .s7panrightbutton { 
bottom:50%; 
margin-bottom:-28px; 
right:0px; 
width:56px; 
height:56px; 
} 
.s7ecatalogviewer .s7ecatrightbutton .s7panrightbutton [state='up'] { 
background-image:url(images/v2/RightButton_dark_up.png); 
} 
.s7ecatalogviewer .s7ecatrightbutton .s7panrightbutton [state='over'] {  
background-image:url(images/v2/RightButton_dark_over.png); 
} 
.s7ecatalogviewer .s7ecatrightbutton .s7panrightbutton [state='down'] {  
background-image:url(images/v2/RightButton_dark_down.png); 
} 
.s7ecatalogviewer .s7ecatrightbutton .s7panrightbutton [state='disabled'] { 
background-image:url(images/v2/RightButton_dark_disabled.png); 
}
```

