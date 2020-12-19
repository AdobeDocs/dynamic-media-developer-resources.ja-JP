---
description: メインスウォッチは、一連のサムネール画像と、左側および右側のオプションのスクロールボタンで構成されます。 スクロールボタンは、デスクトップで、すべてのサムネールがコンテナの幅に収まらない場合にのみ表示されます。 モバイルデバイスの場合や、サムネールがコンテナの幅に収まる場合は、スクロールボタンは表示されません。
seo-description: メインスウォッチは、一連のサムネール画像と、左側および右側のオプションのスクロールボタンで構成されます。 スクロールボタンは、デスクトップで、すべてのサムネールがコンテナの幅に収まらない場合にのみ表示されます。 モバイルデバイスの場合や、サムネールがコンテナの幅に収まる場合は、スクロールボタンは表示されません。
seo-title: メインスウォッチ
solution: Experience Manager
title: メインスウォッチ
topic: Dynamic media
uuid: a968372d-3d11-45d7-b17f-50ec998f5e88
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 2%

---


# メインスウォッチ{#main-swatches}

メインスウォッチは、一連のサムネール画像と、左側および右側のオプションのスクロールボタンで構成されます。 スクロールボタンは、デスクトップで、すべてのサムネールがコンテナの幅に収まらない場合にのみ表示されます。 モバイルデバイスの場合や、サムネールがコンテナの幅に収まる場合は、スクロールボタンは表示されません。

スウォッチコンテナの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7mixedmediaviewer .s7swatches
```

**スウォッチのCSSプロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>スウォッチの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>ビューアのコンテナを基準とする、スウォッチの垂直方向のオフセット。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 高さが100ピクセルのスウォッチを設定するには、次のように記述します。

```
.s7mixedmediviewer .s7swatches { 
 height: 100px;  
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

スウォッチサムネールの間隔は、以下のCSSクラスセレクターを使用して制御します。

`.s7mixedmediaviewer .s7swatches .s7thumbcell`

<table id="table_ECE063DB98154E099FB024F66FF877D7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 各サムネール周囲の水平方向および垂直方向のマージンのサイズ。 実際のサムネールの間隔は、<span class="codeph"> .s7thumbcell </span>に設定された左右のマージンの合計になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**

垂直方向および水平方向に10ピクセルの間隔を設定する場合。

```
.s7mixedmediaviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

個々のサムネールの外観は、以下のCSSクラスセレクターを使用して制御します。

`.s7mixedmediaviewer .s7swatches .s7thumb`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>サムネールの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>サムネールの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p>サムネールの境界線。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>サムネールでは、`state`属性セレクターがサポートされます。このセレクターは、サムネールの状態ごとに異なるスキンを適用するのに使用できます。 具体的には、`state="selected"`はメイン表示に現在表示されている画像のサムネールに対応し、`state="default"`はその他のサムネールに対応し、`state="over"`はマウスカーソルを合わせたときに使用されます。

例 — 56 x 56ピクセルで、初期設定の境界線がライトグレー、選択された境界線がダークグレーのサムネールを設定します。

```
.s7mixedmediaviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7mixedmediaviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7mixedviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

アセットのタイプがサムネール画像の上にオーバーレイされたアイコンとして表示されます。このアイコンは、以下のCSSクラスセレクターを使用して制御します。

`.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay`

<table id="table_460FC57D12CC4B52B3782F4DFAC3A194"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>アイコンオーバーレイの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>アイコンオーバーレイの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

オーバーレイでは、`type`属性セレクターが次の値でサポートされます。`image`（1つの画像の場合）、`swatchset`（スウォッチセットの場合）、`spinset`（スピンセットの場合）、`video`（1つのビデオまたはアダプティブビデオセットの場合）。

例 — スピンセット、スウォッチセットおよびビデオのアイコンオーバーレイを設定するには、次のように記述します。

```
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="swatchset"] { 
 background-image: url(images/v2/ThumbOverlaySwatchSet.png);  
} 
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="spinset"] { 
 background-image: url(images/v2/ThumbOverlaySpinSet.png);  
} 
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="video"] { 
 background-image: url(images/v2/ThumbOverlayVideo.png);  
}
```

左右のスクロールボタンの外観は、以下のCSSクラスセレクターを使用して制御します。

`.s7mixedmediaviewer .s7swatches .s7scrollleftbutton`

`.s7mixedmediaviewer .s7swatches .s7scrollrightbutton`

CSS `top`、`left`、`bottom`および`right`プロパティを使用してスクロールボタンを配置することはできません。 ビューアのロジックによって自動的に配置が決まります。

<table id="table_A5663C4AAC4446168CAD8DBA2894BB9C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>スクロールボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>スクロールボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>ボタンの特定の状態に対して表示する画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、`state`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。`up`、`down`、`over`、および`disabled`。

ボタンのツールヒントをローカライズできます。 詳しくは、[ユーザインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)を参照してください。

例 — 56 x 56ピクセルで、状態ごとに異なるアートワークを持つスクロールボタンを設定するには、次のように記述します。

```
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```

