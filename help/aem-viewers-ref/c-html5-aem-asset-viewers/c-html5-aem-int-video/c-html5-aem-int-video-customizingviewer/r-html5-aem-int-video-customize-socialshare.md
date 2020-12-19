---
description: ソーシャル共有ツールは、デフォルトで右上隅に表示されます。 ボタンと、ユーザーがボタンをクリックまたはタップしたときに展開されるパネルで構成され、個々の共有ツールが含まれます。
seo-description: ソーシャル共有ツールは、デフォルトで右上隅に表示されます。 ボタンと、ユーザーがボタンをクリックまたはタップしたときに展開されるパネルで構成され、個々の共有ツールが含まれます。
seo-title: ソーシャルシェア
solution: Experience Manager
title: ソーシャルシェア
topic: Dynamic media
uuid: 1123e96a-581f-4c1c-ad95-9804e3235002
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 1%

---


# ソーシャルシェア{#social-share}

ソーシャル共有ツールは、デフォルトで右上隅に表示されます。 ボタンと、ユーザーがボタンをクリックまたはタップしたときに展開されるパネルで構成され、個々の共有ツールが含まれます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

ビューアユーザーインターフェイスでのソーシャル共有ツールの位置とサイズは、以下を使用して制御します。

```
.s7interactivevideoviewer .s7socialshare
```

**ソーシャル共有ツールのCSSプロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p> ビューアのコンテナを基準とする、ソーシャル共有ツールの垂直方向の位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左 </span> </p> </td> 
   <td colname="col2"> <p> ビューアのコンテナを基準とする、ソーシャル共有ツールの水平方向の位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> ソーシャル共有ツールの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ソーシャル共有ツールの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example}

ビューアコンテナの上端から4ピクセル、右端から5ピクセルの位置に配置し、サイズが28 x 28ピクセルのソーシャル共有ツールを設定するには、次のように記述します。

```
.s7interactivevideoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

ソーシャル共有ツールボタンの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7interactivevideoviewer .s7socialshare .s7socialbutton
```

**ソーシャル共有ツールボタンのCSSプロパティ**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> ボタンの特定の状態に対して表示する画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、`state`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。

ボタンのツールチップをローカライズできます。 [ユーザインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

## 例 {#example-1}

ボタンの4つの状態ごとに異なる画像を表示するソーシャル共有ツールボタンを設定するには、次のように記述します。

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

個々のソーシャル共有アイコンを含むパネルの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7interactivevideoviewer .s7socialshare .s7socialsharepanel
```

**ソーシャル共有パネルのCSSプロパティ**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>パネルの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example-2}

透明色を持つパネルを設定するには：

```
.s7interactivevideoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```

