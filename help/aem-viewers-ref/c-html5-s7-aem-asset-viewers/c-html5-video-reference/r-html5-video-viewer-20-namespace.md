---
title: Viewer SDK の名前空間
description: Viewer SDK namespace
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: d1f12c9d-9b00-44ee-bd91-76a4d882fecf
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Viewer SDK namespace{#viewer-sdk-namespace}

このビューアは、多くの Viewer SDK コンポーネントで構築されています。 通常、Web ページは、SDK コンポーネント API を直接操作する必要はありません。一般的なニーズはすべて、ビューア API 自体でカバーされています。

However, some advanced use cases require that the web page reference an inner SDK component using the `getComponent()` viewer API and then use all the flexibility of the APIs of the SDK itself.

ビューアが SDK コンポーネントの読み込みと初期化に使用する名前空間は、ビューアの動作環境によって異なります。 ビューアがAdobe Experience Managerで動作している場合、ビューアは、SDK コンポーネントを `s7viewers.s7sdk` 名前空間。 同様に、Dynamic Media Classicから提供されたビューアが SDK をに読み込みます。 `s7classic.s7sdk`.

どちらの場合も、ビューア内の SDK で使用される名前空間には、次のいずれかが含まれます `s7viewers` または `s7classic` というプレフィックスが付きます。 And, it is different from the plain `s7sdk` namespace used in the SDK User Guide or SDK API documentation. そのため、内部のビューアコンポーネントと通信するカスタムアプリケーションコードを記述する際には、完全修飾 SDK 名前空間を使用することが重要です。

例えば、 `StatusEvent.NOTF_VIEW_READY` イベントとビューアがExperience Managerから提供される場合、イベントの完全修飾タイプは `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`を呼び出し、イベントリスナーコードは次のようになります。

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
   videoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for the viewer served from Dynamic Media Classic looks like the following: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
   videoPlayer.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
