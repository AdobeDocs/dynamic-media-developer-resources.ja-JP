---
title: ビデオプレーヤーアイコンエフェクト
description: 再生アイコンがビデオビュー領域にオーバーレイされます。 ビデオが一時停止された場合、またはビデオの終わりに達した場合に表示されます。また、iconeffect パラメーターにも依存します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1e0bd97f-20e9-41e6-95fc-d693644152da
TQID: 'https://experienceleague.adobe.com/LAq8JtRGEkPSrYm5QLGQz6RjhpSSxx7lQcbyaZsIhIw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 177
ht-degree: 0%

---

# ビデオプレーヤーアイコンエフェクト{#video-player-icon-effect}

再生アイコンがビデオビュー領域にオーバーレイされます。 ビデオが一時停止された場合、またはビデオの終わりに達した場合に表示されます。また、iconeffect パラメーターにも依存します。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

再生アイコンの外観は、次のCSS クラスセレクターで制御されます。

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
```

再生アイコンの&#x200B;**CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p> 再生アイコンに表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS スプライト </a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p> 再生アイコンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>再生アイコンの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

アイコンエフェクトは、`state`属性セレクターをサポートしています。 ビデオを再生中に一時停止する場合はセレクター`state="play"`が使用され、再生ヘッドがストリームの最後にある場合は`state="replay"`が使用されます。

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

100 x 100 ピクセル再生アイコンを設定します。

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
