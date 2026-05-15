---
title: Viewer SDK名前空間
description: Viewer SDK名前空間
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ad68dd09-d8df-4fc8-952a-ef82d9662de9
TQID: 'https://experienceleague.adobe.com/U-gO5RmSv5mEWCAPIvJlpp5Fo4PhI0Tws6ZFSOUhtTo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 220
ht-degree: 0%

---

# Viewer SDK名前空間{#viewer-sdk-namespace}

ビューアは、多くのViewer SDK コンポーネントで構築されています。 通常、web ページはSDK コンポーネント APIと直接やり取りする必要はありません。一般的なニーズはすべてビューア API自体でカバーされています。

ただし、一部の高度なユースケースでは、web ページが`getComponent()` ビューア APIを使用してSDK内のコンポーネントを参照し、SDK自体のAPIのすべての柔軟性を使用する必要があります。

ビューアによるSDK コンポーネントの読み込みと初期化に使用される名前空間は、ビューアが動作している環境によって異なります。 ビューアがAdobe Experience Managerで実行されている場合、ビューアはSDK コンポーネントを`s7viewers.s7sdk`名前空間に読み込みます。 同様に、Dynamic Media Classicから提供されたビューアは、SDKを`s7classic.s7sdk`に読み込みます。

いずれの場合も、ビューア内のSDKで使用される名前空間には、接頭辞として`s7viewers`または`s7classic`が含まれています。 また、SDK ユーザーガイドまたはSDK API ドキュメントで使用されているプレーン `s7sdk`名前空間とは異なります。 そのため、内部ビューアコンポーネントと通信するカスタムアプリケーションコードを記述する場合は、完全修飾SDK名前空間を使用することが重要です。

例えば、`StatusEvent.NOTF_VIEW_READY` イベントをリッスンする予定で、ビューアがExperience Managerから提供される場合、完全修飾イベントの種類は`s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`であり、イベントリスナーコードは次のようになります。

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
