---
description: 再生アイコンは、メインビュー領域に重ねて表示されます。 ビデオが一時停止されたとき、またはビデオの終わりに達したときに表示されます。また、iconeffectパラメーターの設定によって表示されます。
solution: Experience Manager
title: アイコンエフェクト
feature: Dynamic Media Classic，ビューア，SDK/API,360 VRビデオ
role: Developer,User
exl-id: e25a3b9d-88ef-4214-9b6b-2527ebf0f145
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---

# アイコンエフェクト{#icon-effect}

再生アイコンは、メインビュー領域に重ねて表示されます。 ビデオが一時停止されたとき、またはビデオの終わりに達したときに表示されます。また、iconeffectパラメーターの設定によって表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

再生アイコンの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7video360viewer . s7video360player .s7iconeffect
```

**再生アイコンのCSSプロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> 再生アイコンに表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合の、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
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

アイコンエフェクトでは、`state`属性セレクターがサポートされます。 `state="play"` は、再生中にビデオが一時停止された場合に使用され、再生ヘッド `state="replay"` がストリームの終わりにある場合に使用されます。

**例**  - 100 x 100ピクセルの再生アイコンを設定します。

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
