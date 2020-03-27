---
description: スウォッチは、一連のサムネール画像と、左側および右側のオプションのスクロールボタンで構成されます。 スクロールボタンは、デスクトップでコンテナの幅にすべてのサムネールが収まらない場合にのみ表示されます。 モバイルデバイスでは、またはサムネールがコンテナの幅に収まる場合、スクロールボタンは表示されません。
seo-description: スウォッチは、一連のサムネール画像と、左側および右側のオプションのスクロールボタンで構成されます。 スクロールボタンは、デスクトップでコンテナの幅にすべてのサムネールが収まらない場合にのみ表示されます。 モバイルデバイスでは、またはサムネールがコンテナの幅に収まる場合、スクロールボタンは表示されません。
seo-title: スウォッチ
solution: Experience Manager
title: スウォッチ
topic: Dynamic media
uuid: d44e775d-5253-4990-98a4-84ff50db09b9
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# スウォッチ{#swatches}

スウォッチは、一連のサムネール画像と、左側および右側のオプションのスクロールボタンで構成されます。 スクロールボタンは、デスクトップでコンテナの幅にすべてのサムネールが収まらない場合にのみ表示されます。 モバイルデバイスでは、またはサムネールがコンテナの幅に収まる場合、スクロールボタンは表示されません。

`.s7zoomviewer .s7swatches`

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

スウォッチコンテナの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7zoomviewer .s7zoomresetbutton
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>スウォッチの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>スウォッチの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>ビューアのコンテナを基準としたスウォッチの垂直方向のオフセット。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — スウォッチを460 x 100ピクセルに設定するには、次のように記述します。

```
.s7zoomviewer .s7swatches { 
 width: 460px; 
 height: 100px;  
}
```

スウォッチサムネールの間隔は、以下のCSSクラスセレクターを使用して制御します。

`.s7zoomviewer .s7swatches .s7thumbcell`

<table id="table_565B354FEA814804A0BE3978E1242110"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 各サムネールの周囲の水平方向および垂直方向のマージンのサイズ。 実際のサムネールの間隔は、.s7thumbcellに設定された左右のマージンの合計 <span class="codeph"> になります </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**

垂直方向および水平方向に10ピクセルの間隔を設定する場合。

```
.s7zoomviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

個々のサムネールの外観は、以下のCSSクラスセレクターを使用して制御します。

`.s7zoomviewer .s7swatches .s7thumb`

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
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
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
>サムネールでは、属性セ `state` レクターがサポートされます。このセレクターは、サムネールの状態ごとに異なるスキンを適用するのに使用できます。 特に、はメイ `state="selected"` ンビューに現在表示されている画像のサムネールに対応し、残りのサムネールに対応し `state="default"` 、マウスカーソルを合わせ `state="over"` たときに使用されます。

例 — 56 x 56ピクセルで、初期設定の境界線がライトグレーで、選択した境界線がダークグレーのサムネールを設定します。

```
.s7zoomviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7zoomviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7zoomviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

左右のスクロールボタンの外観は、以下のCSSクラスセレクターを使用して制御します。

`.s7zoomviewer .s7swatches .s7scrollleftbutton`

`.s7zoomviewer .s7swatches .s7scrollrightbutton`

CSSのtop、left、bottomおよびrightプロパティを使用してスクロールボタンを配置することはできません。 ビューアのロジックによって自動的に配置が決まります。

<table id="table_A5663C4AAC4446168CAD8DBA2894BB9C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>スクロールボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>スクロールボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>特定のボタンの状態で表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p>CSSスプライ <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> トを参照してくだ </a>さい。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、属性セレ `state` クターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。 `up`、 `down`、、 `over`および `disabled`。

ボタンのツールヒントをローカライズできます。 詳しくは、ユー [ザインターフェイス要素のローカリゼーションを参照してくださ](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)い。

例 — 56 x 56ピクセルで、状態ごとに異なるアートワークを持つスクロールボタンを設定します。

```
.s7zoomviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```

