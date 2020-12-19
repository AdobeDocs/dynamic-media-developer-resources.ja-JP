---
description: Twitter共有ツールは、ソーシャル共有パネルに追加されるボタンで構成されます。 ボタンをクリックすると、ソーシャルサービスで提供される共有ダイアログボックスにリダイレクトされます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。
seo-description: Twitter共有ツールは、ソーシャル共有パネルに追加されるボタンで構成されます。 ボタンをクリックすると、ソーシャルサービスで提供される共有ダイアログボックスにリダイレクトされます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。
seo-title: Twitter共有
solution: Experience Manager
title: Twitter共有
topic: Dynamic media
uuid: 609d3c3f-290d-4c21-b61e-70831bee74ea
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# Twitter共有{#twitter-share}

Twitter共有ツールは、ソーシャル共有パネルに追加されるボタンで構成されます。 ボタンをクリックすると、ソーシャルサービスで提供される共有ダイアログボックスにリダイレクトされます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

Twitter共有ボタンの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7twittershare
```

**Twitter共有ツールのCSSプロパティ**

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
   <td colname="col2"> <p> ボタンの特定の状態に対して表示する画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSSスプライト</a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、`state`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。

CSSクラスに`display:none` CSSプロパティを設定すると、ソーシャル共有パネルからボタンを削除できます。

ボタンのツールチップをローカライズできます。 詳しくは、[ユーザインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 — 28 x 28ピクセルで、4つのボタンの状態ごとに異なる画像を表示するTwitter共有ボタンを設定するには、次のように記述します。

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

