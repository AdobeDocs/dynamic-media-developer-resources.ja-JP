---
title: サムネールボタン
description: このボタンを選択すると、メインビューとサムネールの間のビューアの切り替えがリセットされます。 このボタンは、メインコントロールバーに表示されます。 CSS を使用して、このボタンのサイズ、スキン、および配置を設定できます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 465d4320-14ea-4f07-97c0-41f53034a7df
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---

# サムネールボタン{#thumbnails-button}

このボタンを選択すると、メインビューとサムネールの間のビューアの切り替えがリセットされます。 このボタンは、メインコントロールバーに表示されます。 CSS を使用して、このボタンのサイズ、スキン、および配置を設定できます。

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**メインビューア領域の CSS プロパティ**

ボタンの外観は、以下の CSS クラスセレクターを使用して制御します。

`.s7ecatalogsearchviewer .s7thumbnailpagebutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> コントロールバーの上からのオフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> 左側の次のボタンまたはこのボタンが連続する最初のボタンの場合はコントロールバーの左側までの距離。 </p> </td> 
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
   <td colname="col2"> <p>ボタンの特定の状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>関連トピック <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、 `state` および `selected` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。 特に `selected='true'` は、サムネールモードがアクティブな状態のビューアの状態と、 `selected='false'` は、メインビューのデフォルトの状態に対応します。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 — 28 x 28 ピクセルで、メインコントロールバーの下から 4 ピクセル、左端から 5 ピクセルの位置に配置するサムネールボタンを設定します。 最後に、は、選択時または未選択時の 4 つの異なるボタン状態ごとに異なる画像を表示します。

```
.s7ecatalogsearchviewer .s7thumbnailpagebutton{ 
margin-top: 4px; 
margin-left: 5px; width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7thumbnailpagebutton [selected='false'][state='up'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailpagebutton [selected='false'][state='over'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailpagebutton [selected='false'][state='down'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailpagebutton [selected='false'][state='disabled'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_disabled.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailpagebutton [selected='true'][state='up'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailpagebutton [selected='true'][state='over'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailpagebutton [selected='true'][state='down'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailpagebutton [selected='true'][state='disabled'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_disabled.png); 
}
```
