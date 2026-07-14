---
title: 「次のページ」ボタン
description: このボタンを選択すると、ユーザーはカタログ内の次のページに移動します。 このボタンは、メインコントロールバーに表示されます。 このボタンは、画面の不動産を保存するために携帯電話には表示されません。 CSSを使用して、このボタンのサイズ、肌、位置を調整できます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 6b94e583-fb2a-4010-bfc6-4fa901252e4e
TQID: 'https://experienceleague.adobe.com/3qOCJaJs3huicy7sLSoGIQ9dff-VtBom3LM8WLUkETU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 0%

---

# 「次のページ」ボタン{#next-page-button}

このボタンを選択すると、ユーザーはカタログ内の次のページに移動します。 このボタンは、メインコントロールバーに表示されます。 このボタンは、画面の不動産を保存するために携帯電話には表示されません。 CSSを使用して、このボタンのサイズ、肌、位置を調整できます。

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

メイン ビューア領域の&#x200B;**CSS プロパティ**

ボタンの外観は、次のCSS クラスセレクターで制御されます。

`.s7ecatalogsearchviewer .s7toolbarrightbutton .s7panrightbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上位</span> </p> </td> 
   <td colname="col2"> <p>パディングを含むメインコントロールバーの上端からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p>パディングを含むメインコントロールバーの右端からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">さんが</span>を残しました </p> </td> 
   <td colname="col2"> <p>パディングを含むメインコントロールバーの左端からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">下</span> </p> </td> 
   <td colname="col2"> <p>パディングを含むメインコントロールバーの下端からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p>特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるスキンを異なるボタンの状態に適用できます。

ボタンツールのヒントはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 – 次のページボタンを設定するには、28 x 28 ピクセルで、下部から4 ピクセル、メインコントロールバーの右端から250 ピクセルに配置します。 最後に、4つの異なるボタンの状態ごとに異なる画像が表示されます。

```
.s7ecatalogsearchviewer .s7toolbarrightbutton .s7panrightbutton { 
bottom:4px; 
right:250px; 
width:32px; 
height:32px; 
} 
.s7ecatalogsearchviewer .s7toolbarrightbutton .s7panrightbutton [state='up'] { 
background-image:url(images/v2/ToolBarRightButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7toolbarrightbutton .s7panrightbutton [state='over'] {  
background-image:url(images/v2/ToolBarRightButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7toolbarrightbutton .s7panrightbutton [state='down'] {  
background-image:url(images/v2/ToolBarRightButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7toolbarrightbutton .s7panrightbutton [state='disabled'] { 
background-image:url(images/v2/ToolBarRightButton_dark_disabled.png); 
}
```
