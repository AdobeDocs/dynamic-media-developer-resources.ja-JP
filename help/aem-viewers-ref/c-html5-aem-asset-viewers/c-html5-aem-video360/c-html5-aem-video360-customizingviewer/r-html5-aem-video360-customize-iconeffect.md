---
description: 再生アイコンは、メイン表示領域に重ねて表示されます。 ビデオが一時停止したとき、またはビデオの最後に到達したときに表示されます。また、iconeffectパラメーターの設定によって表示されます。
seo-description: 再生アイコンは、メイン表示領域に重ねて表示されます。 ビデオが一時停止したとき、またはビデオの最後に到達したときに表示されます。また、iconeffectパラメーターの設定によって表示されます。
seo-title: アイコンエフェクト
solution: Experience Manager
title: アイコンエフェクト
topic: Dynamic media
uuid: a1e7d877-097c-4f43-8a6d-9627dc4924b1
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# アイコンエフェクト{#icon-effect}

再生アイコンは、メイン表示領域に重ねて表示されます。 ビデオが一時停止したとき、またはビデオの最後に到達したときに表示されます。また、iconeffectパラメーターの設定によって表示されます。

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
   <td colname="col2"> <p> 再生アイコンに表示する画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
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

アイコンエフェクトでは、`state`属性セレクターがサポートされます。 `state="play"` は、再生中にビデオが一時停止されたときに使用され、再生ヘッド `state="replay"` がストリームの最後にあるときに使用されます。

**例** - 100 x 100ピクセルの再生アイコンを設定します。

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

