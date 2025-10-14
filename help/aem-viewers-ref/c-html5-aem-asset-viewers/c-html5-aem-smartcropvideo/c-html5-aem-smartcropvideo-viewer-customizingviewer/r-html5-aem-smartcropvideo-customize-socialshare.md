---
title: ソーシャル共有
description: ソーシャル共有ツールは、デフォルトでは右上隅に表示されます。 ボタンと、ユーザーがボタンをクリックまたはタップすると展開するパネルで構成され、個々の共有ツールが含まれています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 650e1a57-9b0e-4132-a9b0-42c33cacdc04
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# ソーシャル共有{#social-share}

ソーシャル共有ツールは、デフォルトでは右上隅に表示されます。 ボタンと、ユーザーがボタンをクリックまたはタップすると展開するパネルで構成され、個々の共有ツールが含まれています。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

ビューアユーザーインターフェイスのソーシャル共有ツールの位置とサイズは、次のように制御されます。

```
.s7smartcropvideoviewer .s7socialshare
```

**ソーシャル共有ツールの CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 天 </span> </p> </td> 
   <td colname="col2"> <p> ビューアのコンテナを基準とした、ソーシャル共有ツールの垂直方向の位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p> ビューアのコンテナを基準とした、ソーシャル共有ツールの水平方向の位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p> ソーシャル共有ツールの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ソーシャル共有ツールの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – ビューアコンテナの上から 4 ピクセル、右から 5 ピクセルの位置にあり、28 x 28 ピクセルにサイズ設定されるソーシャル共有ツールを設定します。

```
.s7smartcropvideoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

ソーシャル共有ツールボタンの外観は、次の CSS クラスセレクターで制御します。

```
.s7smartcropvideoviewer .s7socialshare .s7socialbutton
```

**ソーシャルボタンの CSS プロパティ**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> ージ </a> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、ボタンの状態に応じて異なるスキンを適用するために使用できる `state` 属性セレクターをサポートしています。

ボタンのツールチップはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 – 4 つの異なるボタンの状態ごとに異なる画像を表示する、ソーシャル共有ツールボタンを設定します。

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

個々のソーシャル共有アイコンを含むパネルの外観は、次の CSS クラスセレクターで制御します。

```
.s7smartcropvideoviewer .s7socialshare .s7socialsharepanel
```

**ソーシャル共有パネルの CSS プロパティ**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>パネルの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – パネルの色を透明に設定する：

```
.s7smartcropvideoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
