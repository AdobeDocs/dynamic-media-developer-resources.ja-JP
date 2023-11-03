---
title: Viewer SDK の名前空間
description: Viewer SDK の名前空間
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ad68dd09-d8df-4fc8-952a-ef82d9662de9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# Viewer SDK の名前空間{#viewer-sdk-namespace}

このビューアは、多くの Viewer SDK コンポーネントで構築されています。 通常、Web ページで SDK コンポーネント API を直接操作する必要はありません。一般的なニーズはすべて、ビューア API 自体で扱われます。

ただし、一部の高度な使用例では、 `getComponent()` ビューア API を使用し、SDK 自体の柔軟な API をすべて使用できます。

ビューアが SDK コンポーネントの読み込みと初期化に使用する名前空間は、ビューアの動作環境によって異なります。 ビューアがAdobe Experience Managerで動作している場合、ビューアは、SDK コンポーネントを `s7viewers.s7sdk` 名前空間。 同様に、Dynamic Media Classicから提供されたビューアが SDK をに読み込みます。 `s7classic.s7sdk`.

どちらの場合も、ビューア内の SDK で使用される名前空間には、次のいずれかが含まれます。 `s7viewers` または `s7classic` というプレフィックスが付きます。 そして平原とは違う `s7sdk` SDK ユーザーガイドまたは SDK API ドキュメントで使用される名前空間です。 そのため、内部のビューアコンポーネントと通信するカスタムアプリケーションコードを記述する際には、完全修飾 SDK 名前空間を使用することが重要です。

例えば、 `StatusEvent.NOTF_VIEW_READY` イベントとビューアがExperience Managerから提供される場合、イベントの完全修飾タイプは `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`を呼び出し、イベントリスナーコードは次のようになります。

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Dynamic Media Classic looks like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
