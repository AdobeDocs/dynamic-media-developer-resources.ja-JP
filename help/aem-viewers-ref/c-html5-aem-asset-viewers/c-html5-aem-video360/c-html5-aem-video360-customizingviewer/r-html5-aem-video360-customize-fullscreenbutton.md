---
description: フルスクリーンボタンをクリックすると、ビデオプレーヤーのフルスクリーンモードが開始または終了します。
solution: Experience Manager
title: フルスクリーンボタン
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
exl-id: 0cb2b1bd-154e-41d8-bd9f-69a1cfc72902
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 2%

---

# フルスクリーンボタン{#full-screen-button}

フルスクリーンボタンをクリックすると、ビデオプレーヤーのフルスクリーンモードが開始または終了します。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

フルスクリーンボタンのサイズ、スキン、およびこのボタンを含むコントロールバーに対する位置を、CSSで設定できます。

フルスクリーンボタンの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7video360viewer .s7fullscreenbutton
```

**フルスクリーンボタンのCSSプロパティ**

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
   <td colname="col1"> <p> <span class="codeph"> 左 </span> </p> </td> 
   <td colname="col2"> <p> パディングを含む左の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>パディングを含む下の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> フルスクリーンボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>フルスクリーンボタンの高さ。 </p> </td> 
  </tr> 
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
>このボタンでは、`state`と`selected`の属性セレクターがサポートされます。これらのセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。 特に、`selected='true'`は「フルスクリーン」の状態に対応し、`selected='false'`は「通常」の状態に対応します。

ボタンのツールチップをローカライズできます。 詳しくは、[ユーザインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)を参照してください。

**例** - 32 x 32ピクセルで、コントロールバーの上および右端から6ピクセルの位置に配置するフルスクリーンボタンを設定します。また、選択時または未選択時のボタンの4つの状態ごとに異なる画像を表示します。

```
.s7video360viewer . s7fullscreenbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7video360viewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7video360viewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7video360viewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7video360viewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7video360viewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7video360viewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7video360viewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7video360viewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```
