---
title: アイコンエフェクト
description: 再生アイコンは、メインビュー領域に重ねて表示されます。 ビデオが一時停止されたとき、またはビデオの最後に達したときに表示されます。また、iconeffect パラメーターの設定によって表示されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e25a3b9d-88ef-4214-9b6b-2527ebf0f145
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 1%

---

# アイコンエフェクト{#icon-effect}

再生アイコンは、メインビュー領域に重ねて表示されます。 ビデオが一時停止されたとき、またはビデオの最後に達したときに表示されます。また、iconeffect パラメーターの設定によって表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

再生アイコンの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7video360viewer . s7video360player .s7iconeffect
```

**再生アイコンの CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> 再生アイコンに表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合の、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a> を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 再生アイコンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>再生アイコンの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

アイコンエフェクトでは、`state` 属性セレクターを使用できます。 属性セレクター `state="play"` は、再生中にビデオが一時停止されたときに使用され、`state="replay"` は再生ヘッドがストリームの最後にあるときに使用されます。

**例**  - 100 x 100 ピクセルの再生アイコンを設定します。

```
.s7video360viewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7video360viewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7video360viewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
