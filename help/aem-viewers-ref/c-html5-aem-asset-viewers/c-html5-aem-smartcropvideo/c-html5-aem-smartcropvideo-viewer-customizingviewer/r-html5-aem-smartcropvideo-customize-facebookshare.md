---
title: Facebook共有
description: Facebook共有ツールは、ソーシャル共有パネルに追加されるボタンで構成されます。 このボタンを選択すると、ソーシャルサービスが提供する共有ダイアログボックスにリダイレクトされます。 ボタンの位置は、Social 共有ツールで完全に管理されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---

# Facebook共有{#facebook-share}

Facebook共有ツールは、ソーシャル共有パネルに追加されるボタンで構成されます。 このボタンを選択すると、ソーシャルサービスが提供する共有ダイアログボックスにリダイレクトされます。 ボタンの位置は、Social 共有ツールで完全に管理されます。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

facebook共有ボタンの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7facebookshare
```

**facebook共有ツールの CSS プロパティ**

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
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>詳しくは、 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、 `state` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。

このボタンを Social 共有パネルから削除するには、 `display:none` CSS プロパティを CSS クラスに設定する。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 — 28 x 28 ピクセルで、4 つのボタンの状態ごとに異なる画像を表示するFacebook共有ボタンを設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7smartcropvideoviewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7smartcropvideoviewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7smartcropvideoviewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```
