---
title: 可変ボリューム
description: 可変ボリュームコントロールは、最初、ユーザーがビデオプレーヤーのサウンドをミュートまたはミュート解除できるボタンとして表示されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: eb30ea49-e0ae-4ef4-a5b3-e245d96ce0db
TQID: 'https://experienceleague.adobe.com/nAeA8SO2K4mcqcfQn9-w1BHZDNlKEGOP0lfEpZH-iWM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 482
ht-degree: 0%

---

# 可変ボリューム{#mutable-volume}

可変ボリュームコントロールは、最初、ユーザーがビデオプレーヤーのサウンドをミュートまたはミュート解除できるボタンとして表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

ユーザーがボタンの上をロールオーバーすると、ユーザーがボリュームを設定できるスライダーが表示されます。 可変ボリュームコントロールは、それを含むコントロールバーに対して、CSSでサイズ、スキン、位置を調整できます。

可変ボリューム領域の外観は、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7mutablevolume
```

可変ボリュームの&#x200B;**CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上位</span> </p> </td> 
   <td colname="col2"> <p> パディングを含む上部境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p> パディングを含む右端からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p> 可変ボリュームコントロールの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>可変ボリュームコントロールの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 可変ボリュームコントロールのカラー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ミュート/ミュート解除ボタンのアピアランスは、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7mutablevolume .s7mutebutton
```

ボタンの状態ごとに背景画像を制御できます。 ボタンのサイズは、ボリュームコントロールのサイズから継承されます。

ボタン画像の&#x200B;**CSS プロパティ**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p> 特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`と`selected`の両方の属性セレクターをサポートしており、異なるスキンを異なるボタンの状態に適用するために使用できます。 特に、`selected='true'`は「ミュート」状態に対応し、`selected='false'`は「ミュート解除」状態に対応します。

垂直方向のボリュームバー領域は、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7mutablevolume .s7verticalvolume
```

**垂直ボリュームバー領域のCSS プロパティ**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 垂直方向のボリュームの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p> 垂直方向のボリュームの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p> 垂直方向のボリュームの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

垂直方向のボリュームコントロール内のトラックは、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7mutablevolume .s7verticalvolume .s7track 
.s7video360viewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

垂直方向のボリュームコントロール内のトラックの&#x200B;**CSS プロパティ**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 垂直方向のボリュームコントロールの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>垂直方向のボリュームコントロールの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>垂直方向のボリューム コントロールの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

垂直方向のボリュームノブは、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7mutablevolume .s7verticalvolume .s7knob
```

垂直方向のボリューム コントロール ノブの&#x200B;**CSS プロパティ**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p> 垂直方向のボリュームコントロールノブアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>垂直方向のボリュームコントロールノブの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>垂直方向のボリューム コントロール ノブの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">さんが</span>を残しました </p> </td> 
   <td colname="col2"> <p>垂直方向のボリュームコントロールノブの水平位置。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ボタンツールのヒントはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)を参照してください。

**例** - 32 x 32 ピクセルで、上から6 ピクセル、コントロールバーの右端から38 ピクセルの位置にあるミュートボタンを設定します。 選択または選択されていない場合は、4つの異なるボタンの状態ごとに異なる画像を表示します。

```
.s7video360viewer .s7mutablevolume { 
top:6px; 
right:38px; 
width:32px; 
height:32px; 
} 
.s7video360viewer .s7mutablevolume .s7mutebutton[selected='true'][state='up'] { 
background-image:url(images/mute_up.png); 
} 
.s7video360viewer .s7mutablevolume .s7mutebutton[selected='true'][state='over'] { 
background-image:url(images/mute_over.png); 
} 
.s7video360viewer .s7mutablevolume .s7mutebutton[selected='true'][state='down'] { 
background-image:url(images/mute_down.png); 
} 
.s7video360viewer .s7mutablevolume .s7mutebutton[selected='true'][state='disabled'] { 
background-image:url(images/mute_disabled.png); 
} 
.s7video360viewer .s7mutablevolume .s7mutebutton[selected='false'][state='up'] { 
background-image:url(images/unmute_up.png); 
} 
.s7video360viewer .s7mutablevolume .s7mutebutton[selected='false'][state='over'] { 
background-image:url(images/unmute_over.png); 
} 
.s7video360viewer .s7mutablevolume .s7mutebutton[selected='false'][state='down'] { 
background-image:url(images/unmute_down.png); 
} 
.s7video360viewer .s7mutablevolume .s7mutebutton[selected='false'][state='disabled'] { 
background-image:url(images/unmute_disabled.png); 
}
```

次に、可変ボリュームコントロール内のボリュームスライダーのスタイル設定の例を示します。

```
.s7video360viewer .s7mutablevolume .s7verticalvolume { 
width:36px; 
height:83px; 
left:0px; 
background-color:#dddddd; 
} 
.s7video360viewer .s7mutablevolume .s7verticalvolume .s7track { 
top:11px; 
left:14px; 
width:10px; 
height:63px; 
background-color:#666666; 
} 
.s7video360viewer .s7mutablevolume .s7verticalvolume .s7filledtrack { 
width:10px; 
background-color:#ababab; 
} 
.s7video360viewer .s7mutablevolume .s7verticalvolume .s7knob { 
width:18px; 
height:10px; 
left:9px; 
background-image:url(images/volumeKnob.png); 
}
```
