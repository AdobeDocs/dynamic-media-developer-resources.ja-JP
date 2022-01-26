---
title: ビデオプレーヤーアイコンエフェクト
description: 再生アイコンは、ビデオ表示領域に重ねて表示されます。 ビデオが一時停止したとき、またはビデオの最後に達したときに表示されます。また、iconeffect パラメーターの設定によって表示されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1e0bd97f-20e9-41e6-95fc-d693644152da
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 1%

---

# ビデオプレーヤーアイコンエフェクト{#video-player-icon-effect}

再生アイコンは、ビデオ表示領域に重ねて表示されます。 ビデオが一時停止したとき、またはビデオの最後に達したときに表示されます。また、iconeffect パラメーターの設定によって表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

再生アイコンの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
```

**再生アイコンの CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 再生アイコンに表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
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

アイコンエフェクトは、 `state` 属性セレクターを使用します。 セレクター `state="play"` は、再生中にビデオが一時停止されたときに使用され、 `state="replay"` は、再生ヘッドがストリームの最後にある場合に使用されます。

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

100 x 100 ピクセルの再生アイコンを設定します。

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
