---
description: このボタンをクリックまたはタップすると、カタログ内の次のページに移動します。 このボタンは、メインコントロールバーに表示されます。 携帯電話では、画面サイズの制限を守るため、このボタンは表示されません。 CSSを使用して、このボタンのサイズ、スキン、位置を設定できます。
seo-description: このボタンをクリックまたはタップすると、カタログ内の次のページに移動します。 このボタンは、メインコントロールバーに表示されます。 携帯電話では、画面サイズの制限を守るため、このボタンは表示されません。 CSSを使用して、このボタンのサイズ、スキン、位置を設定できます。
seo-title: 次の大きいページボタン
solution: Experience Manager
title: 次の大きいページボタン
topic: Dynamic media
uuid: b68332b1-7b6b-46d8-8a0a-aa5a78fca5fb
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 次の大きいページボタン{#large-next-page-button}

このボタンをクリックまたはタップすると、カタログ内の次のページに移動します。 このボタンは、メインコントロールバーに表示されます。 携帯電話では、画面サイズの制限を守るため、このボタンは表示されません。 CSSを使用して、このボタンのサイズ、スキン、位置を設定できます。

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**メインビューア領域のCSSプロパティ**

ボタンの外観は、以下のCSSクラスセレクターを使用して制御します。

`.s7ecatalogsearchviewer .s7ecatrightbutton .s7panrightbutton`

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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>特定のボタンの状態で表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p>CSSスプライトも参 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 照してくださ </a>い。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、属性セレ `state` クターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザインターフェイス要素のローカリゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 — 56 x 56ピクセルで、垂直方向に中央揃えし、ビューアの右の境界線にアンカーし、ボタンの4つの状態ごとに異なる画像を表示する次の大きいページボタンを設定します。

```
.s7ecatalogsearchviewer .s7ecatrightbutton .s7panrightbutton { 
bottom:50%; 
margin-bottom:-28px; 
right:0px; 
width:56px; 
height:56px; 
} 
.s7ecatalogsearchviewer .s7ecatrightbutton .s7panrightbutton [state='up'] { 
background-image:url(images/v2/RightButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7ecatrightbutton .s7panrightbutton [state='over'] {  
background-image:url(images/v2/RightButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7ecatrightbutton .s7panrightbutton [state='down'] {  
background-image:url(images/v2/RightButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7ecatrightbutton .s7panrightbutton [state='disabled'] { 
background-image:url(images/v2/RightButton_dark_disabled.png); 
}
```

