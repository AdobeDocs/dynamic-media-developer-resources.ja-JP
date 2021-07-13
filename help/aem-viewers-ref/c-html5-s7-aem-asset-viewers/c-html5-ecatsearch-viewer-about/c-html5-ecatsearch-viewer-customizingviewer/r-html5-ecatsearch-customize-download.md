---
description: ダウンロード
solution: Experience Manager
title: ダウンロード
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,User
exl-id: eb26ffaa-3c2c-4cee-9a18-f6c5299828c4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 3%

---

# ダウンロード{#download}

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

「ダウンロード」ボタンの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7download
```

**「ダウンロード」ボタンのCSSプロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> コントロールバーの上からのオフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p> 左側の次のボタンまたは（このボタンが行の最初のボタンである場合は）コントロールバーの左側までの距離です。 </p> </td> 
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
   <td colname="col2"> <p> ボタンの特定の状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合の、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSSスプライト</a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、 `state`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 — 28 x 28ピクセルで、ボタンの4つの状態ごとに異なる画像を表示する「ダウンロード」ボタンを設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7download { 
 margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7download[state='up'] { 
background-image:url(images/v2/Dowmload_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7download[state='over'] { 
background-image:url(images/v2/Dowmload_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7download[state='down'] { 
background-image:url(images/v2/Dowmload_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7download[state='disabled'] { 
background-image:url(images/v2/Dowmload_dark_disabled.png); 
}
```
