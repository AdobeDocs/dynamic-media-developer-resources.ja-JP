---
description: Facebook共有ツールは、ソーシャル共有パネルに追加されるボタンで構成されます。 ボタンをクリックすると、ソーシャルサービスで提供される共有ダイアログボックスにリダイレクトされます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。
seo-description: Facebook共有ツールは、ソーシャル共有パネルに追加されるボタンで構成されます。 ボタンをクリックすると、ソーシャルサービスで提供される共有ダイアログボックスにリダイレクトされます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。
seo-title: Facebook共有
solution: Experience Manager
title: Facebook共有
topic: Dynamic media
uuid: 0327631d-9847-409c-bce1-e58ee248d701
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---


# Facebook共有{#facebook-share}

Facebook共有ツールは、ソーシャル共有パネルに追加されるボタンで構成されます。 ボタンをクリックすると、ソーシャルサービスで提供される共有ダイアログボックスにリダイレクトされます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

Facebook共有ボタンの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7videoviewer .s7facebookshare
```

**Facebook共有ツールのCSSプロパティ**

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
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、`state`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。

CSSクラスに`display:none` CSSプロパティを設定すると、ソーシャル共有パネルからボタンを削除できます。

ボタンのツールチップをローカライズできます。 詳しくは、[ユーザインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)を参照してください。

例 — 28 x 28ピクセルで、ボタンの4つの状態ごとに異なる画像を表示するFacebook共有ボタンを設定するには、次のように記述します。

```
.s7videoviewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7videoviewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7videoviewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7videoviewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```

