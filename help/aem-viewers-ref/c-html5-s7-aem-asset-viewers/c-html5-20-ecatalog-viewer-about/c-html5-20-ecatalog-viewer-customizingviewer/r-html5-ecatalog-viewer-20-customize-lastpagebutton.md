---
title: 最後のページボタン
description: このボタンをクリックまたはタップすると、カタログの最後のページに移動します。 このボタンは、デスクトップシステムやタブレットのメインコントロールバーに表示されます。携帯電話では、セカンダリコントロールバーに追加されます。 このボタンのサイズ、スキンおよび位置は、CSS を使用して設定できます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d133a5e2-4a39-41b6-a3fc-9d1b66c78752
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# 最後のページボタン{#last-page-button}

このボタンを選択またはタップすると、カタログの最後のページに移動します。 このボタンは、デスクトップシステムやタブレットのメインコントロールバーに表示されます。携帯電話では、セカンダリコントロールバーに追加されます。 このボタンのサイズ、スキンおよび位置は、CSS を使用して設定できます。

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**メインビューア領域の CSS プロパティ**

ボタンの外観は、次の CSS クラスセレクターで制御します。

`.s7ecatalogviewer .s7lastpagebutton .s7panleftbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 天 </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップシステムやタブレットの場合）またはセカンダリコントロールバー（携帯電話の場合）の上部ボーダーからパディングを含めて配置します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップシステムやタブレットの場合）またはセカンダリコントロールバー（携帯電話の場合）の右端から配置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップシステムやタブレットの場合）またはセカンダリコントロールバー（携帯電話の場合）の左側のボーダーから、パディングを含めて配置します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップシステムやタブレットの場合）またはセカンダリコントロールバー（携帯電話の場合）の下部の境界線からの位置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> ール </a> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、ボタンの状態に応じて異なるスキンを適用するために使用できる `state` 属性セレクターをサポートしています。

ボタンのツールチップはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 – 28 x 28 ピクセルで、メインコントロールバーの下部から 4 ピクセル、左端から 220 ピクセルの「最後のページ」ボタンを設定します。 最後に、は、4 つの異なるボタン状態ごとに異なる画像を表示します。

```
.s7ecatalogviewer .s7lastpagebutton .s7panrightbutton { 
bottom:4px; 
right:220px; 
width:32px; 
height:32px; 
} 
.s7ecatalogviewer .s7lastpagebutton .s7panrightbutton [state='up'] { 
background-image:url(images/v2/LastPageButton_dark_up.png); 
} 
.s7ecatalogviewer .s7lastpagebutton .s7panrightbutton [state='over'] {  
background-image:url(images/v2/LastPageButton_dark_over.png); 
} 
.s7ecatalogviewer .s7lastpagebutton .s7panrightbutton [state='down'] {  
background-image:url(images/v2/LastPageButton_dark_down.png); 
} 
.s7ecatalogviewer .s7lastpagebutton .s7panrightbutton [state='disabled'] { 
background-image:url(images/v2/LastPageButton_dark_disabled.png); 
}
```
