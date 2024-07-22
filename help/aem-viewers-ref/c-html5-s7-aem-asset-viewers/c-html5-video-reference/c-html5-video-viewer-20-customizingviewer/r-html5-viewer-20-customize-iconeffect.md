---
title: アイコン効果
description: 再生アイコンは、メイン表示領域に重ねて表示されます。 これは、ビデオが一時停止されたとき、またはビデオの終わりに達したときに表示されます。また、iconeffect パラメーターにも依存します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: f4bf343a-4a78-470b-abe5-94e2d608f45d
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# アイコン効果{#icon-effect}

再生アイコンは、メイン表示領域に重ねて表示されます。 これは、ビデオが一時停止されたとき、またはビデオの終わりに達したときに表示されます。また、iconeffect パラメーターにも依存します。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

再生アイコンの外観は、次の CSS クラスセレクターで制御します。

```
.s7videoviewer . s7videoplayer .s7iconeffect
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
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト </a> ージ <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> 参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p> 再生アイコンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>再生アイコンの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

アイコン効果では、`state` 属性セレクターがサポートされています。 再生中にビデオが一時停止したときに `state="play"` を使用し、ストリームの最後に再生ヘッドがある場合に `state="replay"` を使用します。

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

100 x 100 ピクセル再生アイコンを設定します。

```
.s7videoviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7videoviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7videoviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
