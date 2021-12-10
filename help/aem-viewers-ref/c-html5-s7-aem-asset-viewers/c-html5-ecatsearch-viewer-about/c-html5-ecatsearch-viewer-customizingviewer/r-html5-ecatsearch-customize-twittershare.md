---
title: Twitter共有
description: Twitter共有ツールは、ソーシャル共有パネルに追加されるボタンで構成されます。 このボタンを選択すると、ソーシャルサービスが提供する共有ダイアログボックスにリダイレクトされます。 ボタンの位置は、Social 共有ツールで完全に管理されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: c7e84d40-a779-4747-b79a-3a40a622a445
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# Twitter共有{#twitter-share}

Twitter共有ツールは、ソーシャル共有パネルに追加されるボタンで構成されます。 このボタンを選択すると、ソーシャルサービスが提供する共有ダイアログボックスにリダイレクトされます。 ボタンの位置は、Social 共有ツールで完全に管理されます。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

twitter共有ボタンの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7twittershare
```

**twitter共有ツールの CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
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
   <td colname="col2"> <p> ボタンの特定の状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>関連トピック <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、 `state` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。

このボタンを Social 共有パネルから削除するには、 `display:none` CSS プロパティを CSS クラスに設定する。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 — 28 x 28 ピクセルで、4 つのボタンの状態ごとに異なる画像を表示するTwitter共有ボタンを設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```
