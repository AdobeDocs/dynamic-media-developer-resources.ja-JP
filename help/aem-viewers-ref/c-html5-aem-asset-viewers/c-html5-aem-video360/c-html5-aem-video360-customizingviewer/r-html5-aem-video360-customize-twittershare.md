---
title: Twitter共有
description: Twitter共有ツールは、ソーシャル共有パネルに追加されるボタンで構成されます。 このボタンを選択すると、ソーシャルサービスで提供される共有ダイアログボックスにリダイレクトされます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: a90a4c82-b51a-4fb0-9196-44ae4ba8e0cd
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Twitter共有{#twitter-share}

Twitter共有ツールは、ソーシャル共有パネルに追加されるボタンで構成されます。 このボタンを選択すると、ソーシャルサービスで提供される共有ダイアログボックスにリダイレクトされます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

twitter共有ボタンの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7video360viewer .s7twittershare
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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> 特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合の、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a> を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、 `state` 属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。

CSS クラスで `display:none` CSS プロパティを設定することで、このボタンをソーシャル共有パネルから削除できます。

ボタンのツールチップはローカライズできます。 [ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) を参照してください。

**例**  - 28 x 28 ピクセルで、4 つのボタンの状態ごとに異なる画像を表示するTwitter共有ボタンを設定するには：

```
.s7video360viewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7video360viewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7video360viewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7video360viewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```
