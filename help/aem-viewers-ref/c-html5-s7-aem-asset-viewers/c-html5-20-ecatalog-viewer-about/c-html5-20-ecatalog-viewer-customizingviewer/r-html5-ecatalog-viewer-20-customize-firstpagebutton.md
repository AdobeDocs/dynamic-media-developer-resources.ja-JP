---
title: 最初のページボタン
description: このボタンをクリックまたはタップすると、カタログの最初のページに移動します。 このボタンは、デスクトップシステムおよびタブレットのメインコントロールバーに表示されます。携帯電話では、セカンダリコントロールバーに追加されます。 CSS を使用して、このボタンのサイズ、スキン、および配置を設定できます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 50ebf51f-aa51-4778-8956-f969c30443aa
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 2%

---

# 最初のページボタン{#first-page-button}

このボタンを選択またはタップすると、カタログの最初のページに移動します。 このボタンは、デスクトップシステムおよびタブレットのメインコントロールバーに表示されます。携帯電話では、セカンダリコントロールバーに追加されます。 CSS を使用して、このボタンのサイズ、スキン、および配置を設定できます。

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**メインビューア領域の CSS プロパティ**

ボタンの外観は、以下の CSS クラスセレクターを使用して制御します。

`.s7ecatalogviewer .s7firstpagebutton .s7panleftbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップシステムおよびタブレットの場合）またはセカンダリコントロールバー（携帯電話の場合）の上の境界線からの位置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップシステムおよびタブレットの場合）またはセカンダリコントロールバー（携帯電話の場合）の右の境界線からの位置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左 </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップシステムおよびタブレットの場合）またはセカンダリコントロールバー（携帯電話の場合）の左の境界線からの位置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップシステムおよびタブレットの場合）またはセカンダリコントロールバー（携帯電話の場合）の下の境界線からの位置（パディングを含む）。 </p> </td> 
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
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>関連トピック <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、 `state` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 — 28 x 28 ピクセルで、メインコントロールバーの下から 4 ピクセル、左端から 220 ピクセルの位置に配置する最初のページボタンを設定するには、次のように記述します。 最後に、は 4 つのボタンの状態ごとに異なる画像を表示します。

```
.s7ecatalogviewer .s7firstpagebutton .s7panleftbutton { 
bottom:4px; 
left:220px; 
width:32px; 
height:32px; 
} 
.s7ecatalogviewer .s7firstpagebutton .s7panleftbutton [state='up'] { 
background-image:url(images/v2/FirstPageButton_dark_up.png); 
} 
.s7ecatalogviewer .s7firstpagebutton .s7panleftbutton [state='over'] {  
background-image:url(images/v2/FirstPageButton_dark_over.png); 
} 
.s7ecatalogviewer .s7firstpagebutton .s7panleftbutton [state='down'] {  
background-image:url(images/v2/FirstPageButton_dark_down.png); 
} 
.s7ecatalogviewer .s7firstpagebutton .s7panleftbutton [state='disabled'] { 
background-image:url(images/v2/FirstPageButton_dark_disabled.png); 
}
```
