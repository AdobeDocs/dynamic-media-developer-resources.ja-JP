---
title: スピン右ボタン
description: このボタンをクリックまたはタップすると、メインビューで画像が右にスピンします。 このボタンは、画面の領域を節約するために携帯電話には表示されません。 また、多次元スピンセットを使用すると、ボタンは非表示になります。 CSS を使用して、ボタンのサイズ、スキンおよび位置を設定できます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 2e70ad27-9fce-4a18-b856-08aa6dbec3f2
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# スピン右ボタン{#spin-right-button}

このボタンを選択すると、メインビューで画像が右にスピンします。 このボタンは、画面の領域を節約するために携帯電話には表示されません。 また、多次元スピンセットを使用すると、ボタンは非表示になります。 CSS を使用して、ボタンのサイズ、スキンおよび位置を設定できます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**スピンボタンの CSS プロパティ**

ボタンが、CSS クラスセレクターで DIV 制御される内部コンテナに追加されます。

```
.s7mixedmediaviewer .s7spinbuttons
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
   <td colname="col1"> <p> <span class="codeph"> 天 </span> </p> </td> 
   <td colname="col2"> <p>上部のボーダーから配置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>パディングを含めて、右側のボーダーから配置します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>パディングを含めて、左のボーダーから配置します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>下罫線からパディングを含めて移動します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

コンテナ内でのこのボタンの外観は、CSS クラスセレクターで制御します。

```
.s7mixedmediaviewer .s7spinbuttons .s7panrightbutton
```

<table id="table_3EC45539877A479DB83E8FC69142450B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 天 </span> </p> </td> 
   <td colname="col2"> <p>上部のボーダーから配置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>パディングを含めて、右側のボーダーから配置します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>パディングを含めて、左のボーダーから配置します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>下罫線からパディングを含めて移動します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト </a> ージ <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、ボタンの状態に応じて異なるスキンを適用するために使用できる `state` 属性セレクターをサポートしています。

ボタンのツールチップはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) を参照してください。

例 – 28 x 28 ピクセルのスピン Right ボタンを設定し、内部コンテナの右端に配置する 最後に、は、4 つの異なるボタン状態ごとに異なる画像を表示します。

```
.s7mixedmediaviewer .s7spinbuttons .s7panrightbutton { 
 position:absolute; 
 right: 0px; 
 width:28px; 
 height:28px; 
 background-size:contain; 
 } 
.s7mixedmediaviewer .s7spinbuttons .s7panrightbutton[state='up'] { 
background-image:url(images/v2/SpinRightButton_light_up.png); 
} 
.s7mixedmediaviewer .s7spinbuttons .s7panrightbutton[state='over'] { 
background-image:url(images/v2/SpinRightButton_light_over.png); 
} 
.s7mixedmediaviewer .s7spinbuttons .s7panrightbutton[state='down'] { 
 background-image:url(images/v2/SpinRightButton_light_down.png); 
} 
.s7mixedmediaviewer .s7spinbuttons .s7panrightbutton[state='disabled'] { 
 background-image:url(images/v2/SpinRightButton_light_disabled.png); 
}
```
