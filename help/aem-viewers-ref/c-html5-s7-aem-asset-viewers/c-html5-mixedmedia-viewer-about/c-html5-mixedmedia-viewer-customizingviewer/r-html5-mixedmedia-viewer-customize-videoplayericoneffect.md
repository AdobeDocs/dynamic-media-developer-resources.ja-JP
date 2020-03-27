---
description: 再生アイコンは、ビデオビュー領域に重ねて表示されます。 ビデオが一時停止されたとき、またはビデオの最後に到達したときに表示されます。また、iconeffectパラメーターの設定によっても表示されます。
seo-description: 再生アイコンは、ビデオビュー領域に重ねて表示されます。 ビデオが一時停止されたとき、またはビデオの最後に到達したときに表示されます。また、iconeffectパラメーターの設定によっても表示されます。
seo-title: ビデオプレーヤーアイコンエフェクト
solution: Experience Manager
title: ビデオプレーヤーアイコンエフェクト
topic: Dynamic media
uuid: 5d59c4b2-a7a1-49e1-84c7-0e127a571c4f
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# ビデオプレーヤーアイコンエフェクト{#video-player-icon-effect}

再生アイコンは、ビデオビュー領域に重ねて表示されます。 ビデオが一時停止されたとき、またはビデオの最後に到達したときに表示されます。また、iconeffectパラメーターの設定によっても表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

再生アイコンの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
```

**再生アイコンのCSSプロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 再生アイコンに表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p>CSSスプライ <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> トを参照してくだ </a>さい。 </p> </td> 
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

アイコンエフェクトは、属性セレクター `state` をサポートします。 `state="play"` は、ビデオが再生中に一時停止されたときに使用され、再生ヘ `state="replay"` ッドがストリームの最後にあるときに使用されます。

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

100 x 100ピクセルの再生アイコンを設定します。

```
.s7mixedmediaviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```

