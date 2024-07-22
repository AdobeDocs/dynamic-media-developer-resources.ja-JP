---
title: アイコン効果
description: 再生アイコンは、メイン表示領域に重ねて表示されます。 これは、ビデオが一時停止されたとき、またはビデオの終わりに達したときに表示されます。また、iconeffect パラメーターにも依存します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e25a3b9d-88ef-4214-9b6b-2527ebf0f145
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# アイコン効果{#icon-effect}

再生アイコンは、メイン表示領域に重ねて表示されます。 これは、ビデオが一時停止されたとき、またはビデオの終わりに達したときに表示されます。また、iconeffect パラメーターにも依存します。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

再生アイコンの外観は、次の CSS クラスセレクターで制御します。

```
.s7video360viewer . s7video360player .s7iconeffect
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
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト </a> ージ <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> 参照してください。 </p> </td> 
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

アイコン効果では、`state` 属性セレクターがサポートされています。 属性セレクター `state="play"` は、再生中にビデオを一時停止した場合に使用さ `state="replay"`、再生ヘッドがストリームの最後にある場合に使用されます。

**例** - 100 x 100 ピクセル再生アイコンの設定。

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
