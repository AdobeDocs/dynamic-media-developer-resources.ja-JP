---
title: ソーシャル共有
description: ソーシャル共有ツールは、デフォルトで右上隅に表示されます。 このツールは、ボタンと、ユーザーがボタンをクリックまたはタップしたときに展開するパネルで構成され、個々の共有ツールが含まれます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 82b482f9-b117-4529-a422-cdb0eead0031
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 1%

---

# ソーシャル共有{#social-share}

ソーシャル共有ツールは、デフォルトで右上隅に表示されます。 このツールは、ボタンと、ユーザーがボタンをクリックまたはタップしたときに展開するパネルで構成され、個々の共有ツールが含まれます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

ビューアのユーザーインターフェイスでのソーシャル共有ツールの位置とサイズは、次の方法で制御します。

```
.s7smartcropvideoviewer .s7socialshare
```

**ソーシャル共有ツールの CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p> ビューアのコンテナを基準とした、ソーシャル共有ツールの垂直方向の位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左 </span> </p> </td> 
   <td colname="col2"> <p> ビューアのコンテナを基準とした、ソーシャル共有ツールの水平方向の位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> ソーシャル共有ツールの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ソーシャル共有ツールの高さです。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — ビューアのコンテナの上から 4 ピクセル、右から 5 ピクセルの位置に配置し、サイズが 28 x 28 ピクセルのソーシャル共有ツールを設定します。

```
.s7smartcropvideoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

ソーシャル共有ツールボタンの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7socialshare .s7socialbutton
```

**ソーシャルボタンの CSS プロパティ**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
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

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 — ボタンの 4 つの状態ごとに異なる画像を表示するソーシャル共有ツールボタンを設定します。

```
.s7smartcropvideoviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7smartcropvideoviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7smartcropvideoviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7smartcropvideoviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

個々のソーシャル共有アイコンを含むパネルの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7socialshare .s7socialsharepanel
```

**ソーシャル共有パネルの CSS プロパティ**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>パネルの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 透明色を持つパネルを設定します。

```
.s7smartcropvideoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
