---
title: スウォッチ
description: スウォッチは、サムネール画像の行と、左右にオプションのスクロールボタンで構成されます。 スクロール ボタンは、すべてのサムネールがコンテナの幅に収まらない場合にのみ、デスクトップに表示されます。 モバイルデバイスで、またはサムネールがコンテナの幅に収まる場合、スクロールボタンが表示されません。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 7eaa4a6e-98e8-477b-9f45-66f8a79dfd85
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 0%

---

# スウォッチ{#swatches}

スウォッチは、サムネール画像の行と、左右にオプションのスクロールボタンで構成されます。 スクロール ボタンは、すべてのサムネールがコンテナの幅に収まらない場合にのみ、デスクトップに表示されます。 モバイルデバイスで、またはサムネールがコンテナの幅に収まる場合、スクロールボタンが表示されません。

`.s7zoomviewer .s7swatches`

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域の CSS プロパティ**

スウォッチコンテナの外観は、次の CSS クラスセレクターで制御します。

```
.s7zoomviewer .s7zoomresetbutton
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>スウォッチの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>スウォッチの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>ビューアコンテナを基準とした垂直方向のスウォッチのオフセット。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – スウォッチを 460 x 100 ピクセルに設定する

```
.s7zoomviewer .s7swatches { 
 width: 460px; 
 height: 100px;  
}
```

スウォッチサムネール間の間隔は、次の CSS クラスセレクターで制御します。

`.s7zoomviewer .s7swatches .s7thumbcell`

<table id="table_565B354FEA814804A0BE3978E1242110"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 各サムネールの周囲の水平方向と垂直方向の余白のサイズ。 実際のサムネールの間隔は、.s7thumbcell <span class="codeph"> に設定されている左右の余白 </span> 合計と等しくなります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**

垂直方向と水平方向の両方で 10 ピクセルに間隔を設定します。

```
.s7zoomviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

個々のサムネールの外観は、次の CSS クラスセレクターで制御します。

`.s7zoomviewer .s7swatches .s7thumb`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>サムネールの幅 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>サムネールの高さ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 境界線 </span> </p> </td> 
   <td colname="col2"> <p>サムネールのボーダー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>サムネールでは `state` 属性セレクターがサポートされており、これを使用して異なるスキンを異なるサムネール状態に適用できます。 特に、`state="selected"` は、現在メインビューに表示されている画像のサムネールに対応 `state="default"`、残りのサムネールに対応し、マウスのカーソルを合わせ `state="over"` ときに使用されます。

例 – 56 x 56 ピクセルのサムネールで、デフォルトの境界線が薄いグレーになり、選択した境界線が濃いグレーになるようにします。

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

左右のスクロールボタンの外観は、次の CSS クラスセレクターで制御します。

`.s7zoomviewer .s7swatches .s7scrollleftbutton`

`.s7zoomviewer .s7swatches .s7scrollrightbutton`

CSS の top、left、bottom、right プロパティを使用してスクロールボタンを配置することはできません。 代わりに、ビューアロジックによって自動的に配置されます。

<table id="table_A5663C4AAC4446168CAD8DBA2894BB9C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>スクロールボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>スクロール ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> ージ </a> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`、`up`、`down`、`over` などの異なるボタン状態に異なるスキンを適用するために使用できる `disabled` 属性セレクターをサポートしています。

ボタンのツールチップはローカライズできます。 [&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 – 56 x 56 ピクセルで、状態ごとに異なるアートワークを持つスクロールボタンを設定する場合

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
