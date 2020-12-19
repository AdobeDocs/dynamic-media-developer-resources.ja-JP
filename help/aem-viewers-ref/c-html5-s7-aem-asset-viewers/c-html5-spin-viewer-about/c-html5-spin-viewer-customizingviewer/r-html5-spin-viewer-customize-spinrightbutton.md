---
description: このボタンをクリックまたはタップすると、メイン表示の画像が右方向にスピンします。 携帯電話では、画面サイズの制限を守るため、このボタンは表示されません。 また、複数次元のスピンセットを使用する場合は、このボタンが非表示になります。 CSSを使用して、ボタンのサイズ設定、スキン表示および配置を行うことができます。
seo-description: このボタンをクリックまたはタップすると、メイン表示の画像が右方向にスピンします。 携帯電話では、画面サイズの制限を守るため、このボタンは表示されません。 また、複数次元のスピンセットを使用する場合は、このボタンが非表示になります。 CSSを使用して、ボタンのサイズ設定、スキン表示および配置を行うことができます。
seo-title: 右へスピンボタン
solution: Experience Manager
title: 右へスピンボタン
topic: Dynamic media
uuid: 5c754e53-9311-4d4f-96e7-2bb9a5a7babf
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 3%

---


# 右へスピンボタン{#spin-right-button}

このボタンをクリックまたはタップすると、メイン表示の画像が右方向にスピンします。 携帯電話では、画面サイズの制限を守るため、このボタンは表示されません。 また、複数次元のスピンセットを使用する場合は、このボタンが非表示になります。 CSSを使用して、ボタンのサイズ設定、スキン表示および配置を行うことができます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**スピンボタンのCSSプロパティ**

ボタンが内部コンテナ(DIV)に追加されます。この内部セレクターは、CSSクラスセレクターを使用して制御します。

```
.s7spinviewer .s7spinbuttons
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
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p>パディングを含む上の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>パディングを含む右の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左 </span> </p> </td> 
   <td colname="col2"> <p>パディングを含む左の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>パディングを含む下の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

コンテナ内でのこのボタンの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7spinviewer .s7spinbuttons .s7panrightbutton
```

<table id="table_3EC45539877A479DB83E8FC69142450B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p>パディングを含む上の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>パディングを含む右の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左 </span> </p> </td> 
   <td colname="col2"> <p>パディングを含む左の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>パディングを含む下の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>ボタンの特定の状態に対して表示する画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p>CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#section-b671c70acf284cb0aea678c2d2e4babc" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、`state`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。

ボタンのツールチップをローカライズできます。 詳しくは、[ユーザインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98)を参照してください。

例 — 28 x 28ピクセルで、内側のコンテナの右端に配置し、ボタンの4つの状態ごとに異なる画像を表示する右へスピンボタンを設定するには、次のように記述します。

```
.s7spinviewer .s7spinbuttons .s7panrightbutton { 
 position:absolute; 
 right: 0px; 
 width:28px; 
 height:28px; 
 background-size:contain; 
 } 
.s7spinviewer .s7spinbuttons .s7panrightbutton[state='up'] { 
background-image:url(images/v2/SpinRightButton_light_up.png); 
} 
.s7spinviewer .s7spinbuttons .s7panrightbutton[state='over'] { 
background-image:url(images/v2/SpinRightButton_light_over.png); 
} 
.s7spinviewer .s7spinbuttons .s7panrightbutton[state='down'] { 
 background-image:url(images/v2/SpinRightButton_light_down.png); 
} 
.s7spinviewer .s7spinbuttons .s7panrightbutton[state='disabled'] { 
 background-image:url(images/v2/SpinRightButton_light_disabled.png); 
}
```

