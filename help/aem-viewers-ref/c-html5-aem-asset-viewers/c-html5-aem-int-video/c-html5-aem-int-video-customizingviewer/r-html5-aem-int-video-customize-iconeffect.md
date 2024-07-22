---
title: アイコン効果
description: 再生アイコンは、メイン表示領域に重ねて表示されます。 これは、ビデオが一時停止されたとき、またはビデオの終わりに達したときに表示されます。また、iconeffect パラメーターにも依存します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: bbb35286-fdb6-4329-a837-17fe8f976276
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# アイコン効果{#icon-effect}

再生アイコンは、メイン表示領域に重ねて表示されます。 これは、ビデオが一時停止されたとき、またはビデオの終わりに達したときに表示されます。また、iconeffect パラメーターにも依存します。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

再生アイコンの外観は、次の CSS クラスセレクターで制御します。

```
.s7interactivevideoviewer . s7videoplayer .s7iconeffect
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
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト </a> ージ <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> 参照してください。 </p> </td> 
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

アイコン効果では、`state` 属性セレクターがサポートされています。 属性 `state="play"` は、再生中にビデオを一時停止した場合に使用さ `state="replay"`、再生ヘッドがストリームの最後にある場合に使用されます。

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

100 x 100 ピクセル再生アイコンを設定します。

```
.s7interactivevideoviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7interactivevideoviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7interactivevideoviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
