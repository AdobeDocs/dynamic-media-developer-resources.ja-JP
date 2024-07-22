---
title: ソーシャル共有
description: ソーシャル共有ツールは、デフォルトでは右上隅に表示されます。 ボタンと、ユーザーがボタンをクリックまたはタップすると展開するパネルで構成され、個々の共有ツールが含まれています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: ad544a12-d2a4-45c9-9e76-e0bf96901725
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# ソーシャル共有{#social-share}

ソーシャル共有ツールは、デフォルトでは右上隅に表示されます。 ボタンと、ユーザーがボタンをクリックまたはタップすると展開するパネルで構成され、個々の共有ツールが含まれています。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

ビューアユーザーインターフェイスのソーシャル共有ツールの位置とサイズは、次のように制御されます。

```
.s7interactivevideoviewer .s7socialshare
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

## 例 {#example}

ビューアコンテナの上から 4 ピクセル、右から 5 ピクセルの位置に 28×28 ピクセルのサイズのソーシャル共有ツールを設定する。

```
.s7interactivevideoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

ソーシャル共有ツールボタンの外観は、次の CSS クラスセレクターで制御します。

```
.s7interactivevideoviewer .s7socialshare .s7socialbutton
```

**ソーシャル共有ツールボタンの CSS プロパティ**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト </a> ージ <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、ボタンの状態に応じて異なるスキンを適用するために使用できる `state` 属性セレクターをサポートしています。

ボタンのツールチップはローカライズできます。 [ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

## 例 {#example-1}

4 つの異なるボタン状態ごとに異なる画像を表示するソーシャル共有ツールボタンを設定する。

```
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

個々のソーシャル共有アイコンを含むパネルの外観は、次の CSS クラスセレクターで制御します。

```
.s7interactivevideoviewer .s7socialshare .s7socialsharepanel
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

## 例 {#example-2}

パネルを透過色に設定するには：

```
.s7interactivevideoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
