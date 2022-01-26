---
title: 可変ボリューム
description: ミュート可能ボリュームコントロールは、最初は、ユーザーがビデオプレーヤーのサウンドをミュートまたはミュート解除するボタンとして表示されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 9afa56f9-443c-4307-843c-d7ddba6ec604
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 2%

---

# 可変ボリューム{#mutable-volume}

ミュート可能ボリュームコントロールは、最初は、ユーザーがビデオプレーヤーのサウンドをミュートまたはミュート解除するボタンとして表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

ユーザーがボタンの上にロールオーバーすると、スライダが表示され、ボリュームを設定できます。 可変ボリュームコントロールは、CSS を使用して、そのコントロールバーを基準にして、サイズ変更、スキン、配置を行うことができます。

可変ボリューム領域の外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7mixedmediaviewer .s7mutablevolume
```

**可変ボリュームの CSS プロパティ**

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
   <td colname="col2"> <p> 可変ボリュームコントロールの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>可変ボリュームコントロールの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 可変ボリュームコントロールの色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ミュート/ミュート解除ボタンの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton
```

ボタンの状態ごとに背景画像を制御できます。 ボタンのサイズは、ボリュームコントロールのサイズから継承されます。

**ボタン画像の CSS プロパティ**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、 `state` および `selected` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。 特に `selected='true'` は「ミュート」状態に対応し、 `selected='false'` は、「ミュート解除済み」の状態に対応します。

垂直ボリュームバー領域は、以下の CSS クラスセレクターを使用して制御します。

```
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume
```

**垂直ボリュームバー領域の CSS プロパティ**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 垂直ボリュームの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p> 垂直ボリュームの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p> 垂直ボリュームの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

垂直ボリュームコントロール内のトラックは、以下の CSS クラスセレクターを使用して制御します。

```
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume .s7track 
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**垂直ボリュームコントロールの CSS プロパティ**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 垂直ボリュームコントロールの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>垂直ボリュームコントロールの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>垂直ボリュームコントロールの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

垂直ボリュームノブは、以下の CSS クラスセレクターを使用して制御します。

```
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume .s7knob
```

**垂直ボリュームコントロールノブの CSS プロパティ**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 垂直ボリュームコントロールノブのアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>垂直ボリュームコントロールノブの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>垂直ボリュームコントロールノブの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左 </span> </p> </td> 
   <td colname="col2"> <p>垂直ボリュームコントロールノブの水平方向の位置。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) を参照してください。

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

32 x 32 ピクセルで、コントロールバーの上から 6 ピクセル、右端から 38 ピクセルの位置に配置するミュートボタンを設定するには、次のように記述します。 選択時または未選択時の 4 つのボタンの状態ごとに異なる画像を表示します。

```
.s7mixedmediaviewer .s7mutablevolume { 
top:6px; 
right:38px; 
width:32px; 
height:32px; 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='true'][state='up'] { 
background-image:url(images/mute_up.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='true'][state='over'] { 
background-image:url(images/mute_over.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='true'][state='down'] { 
background-image:url(images/mute_down.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='true'][state='disabled'] { 
background-image:url(images/mute_disabled.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='false'][state='up'] { 
background-image:url(images/unmute_up.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='false'][state='over'] { 
background-image:url(images/unmute_over.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='false'][state='down'] { 
background-image:url(images/unmute_down.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='false'][state='disabled'] { 
background-image:url(images/unmute_disabled.png); 
}
```

次の例は、可変ボリュームコントロール内のボリュームスライダのスタイルを設定する方法を示しています。

```
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume { 
width:36px; 
height:83px; 
left:0px; 
background-color:#dddddd; 
} 
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume .s7track { 
top:11px; 
left:14px; 
width:10px; 
height:63px; 
background-color:#666666; 
} 
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume .s7filledtrack { 
width:10px; 
background-color:#ababab; 
} 
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume .s7knob { 
width:18px; 
height:10px; 
left:9px; 
background-image:url(images/volumeKnob.png); 
}
```
