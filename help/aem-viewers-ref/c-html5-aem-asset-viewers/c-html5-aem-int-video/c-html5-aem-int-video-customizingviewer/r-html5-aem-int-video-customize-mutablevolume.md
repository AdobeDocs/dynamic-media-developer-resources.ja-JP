---
description: ミュート可能ボリュームコントロールは、最初はボタンとして表示され、ユーザがビデオプレーヤーの音をミュートまたはミュート解除できます。
solution: Experience Manager
title: ミュート可能ボリューム
feature: Dynamic Mediaクラシック，ビューア，SDK/API，インタラクティブビデオ
role: 開発者、業務従事者
exl-id: ecef47c1-e659-4930-bfb1-cc5e7c059094
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 2%

---

# ミュート可能ボリューム{#mutable-volume}

ミュート可能ボリュームコントロールは、最初はボタンとして表示され、ユーザがビデオプレーヤーの音をミュートまたはミュート解除できます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

ユーザーがボタンをロールオーバーすると、スライダーが表示され、ボリュームを設定できます。 ミュート可能ボリュームコントロールは、CSSを使用して、このコントロールを含むコントロールバーに対するサイズ、スキン、および位置を設定できます。

ミュート可能ボリューム領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7interactivevideoviewer .s7mutablevolume
```

**ミュート可能ボリュームのCSSプロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p> パディングを含む上の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p> パディングを含む右の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> ミュート可能ボリュームコントロールの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ミュート可能ボリュームコントロールの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> ミュート可能ボリュームコントロールのカラー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ミュート/ミュート解除ボタンの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton
```

ボタンの状態ごとに背景画像を制御できます。 ボタンのサイズは、ボリュームコントロールのサイズから継承されます。

**ボタン画像のCSSプロパティ**

<table id="table_46903DCACF314426B67783167ADF7715"> 
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
>このボタンでは、`state`と`selected`の属性セレクターがサポートされます。これらのセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。 特に、`selected='true'`は「ミュート」状態に対応し、`selected='false'`は「ミュート解除」状態に対応します。

垂直ボリュームバー領域は、以下のCSSクラスセレクターを使用して制御します。

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume
```

**垂直ボリュームバー領域のCSSプロパティ**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 垂直ボリュームの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> 垂直ボリュームの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p> 垂直ボリュームの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

垂直ボリュームコントロール内のトラックは、以下のCSSクラスセレクターを使用して制御します。

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7track 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**垂直ボリュームコントロール内のトラックのCSSプロパティ**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 垂直ボリュームコントロールの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>垂直ボリュームコントロールの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>垂直ボリュームコントロールの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

垂直ボリュームノブは、以下のCSSクラスセレクターを使用して制御します。

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7knob
```

**垂直ボリュームコントロールノブのCSSプロパティ**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> 垂直ボリュームコントロールノブのアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>垂直ボリュームコントロールノブの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>垂直ボリュームコントロールノブの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左 </span> </p> </td> 
   <td colname="col2"> <p>垂直ボリュームコントロールノブの水平方向の位置。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ボタンのツールチップをローカライズできます。 詳しくは、[ユーザインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

32 x 32ピクセルで、コントロールバーの上から6ピクセル、右端から38ピクセルの位置に配置するミュートボタンを設定します。 選択時または未選択時のボタンの4つの状態ごとに異なる画像を表示します。

```
.s7interactivevideoviewer .s7mutablevolume { 
top:6px; 
right:38px; 
width:32px; 
height:32px; 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='up'] { 
background-image:url(images/mute_up.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='over'] { 
background-image:url(images/mute_over.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='down'] { 
background-image:url(images/mute_down.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='disabled'] { 
background-image:url(images/mute_disabled.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='up'] { 
background-image:url(images/unmute_up.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='over'] { 
background-image:url(images/unmute_over.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='down'] { 
background-image:url(images/unmute_down.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='disabled'] { 
background-image:url(images/unmute_disabled.png); 
}
```

ミュート可能ボリュームコントロール内のボリュームスライダのスタイル設定の例を以下に示します。

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume { 
width:36px; 
height:83px; 
left:0px; 
background-color:#dddddd; 
} 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7track { 
top:11px; 
left:14px; 
width:10px; 
height:63px; 
background-color:#666666; 
} 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack { 
width:10px; 
background-color:#ababab; 
} 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7knob { 
width:18px; 
height:10px; 
left:9px; 
background-image:url(images/volumeKnob.png); 
}
```
