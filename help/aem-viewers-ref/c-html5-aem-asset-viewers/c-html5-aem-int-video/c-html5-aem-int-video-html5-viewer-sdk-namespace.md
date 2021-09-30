---
title: ビューアSDKの名前空間
description: ビューアSDKの名前空間
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 4a4d821e-9351-4efa-8849-968e746911f3
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# ビューアSDKの名前空間{#viewer-sdk-namespace}

このビューアは、多くのビューアSDKコンポーネントで構築されています。 通常、WebページでSDKコンポーネントAPIを直接操作する必要はありません。一般的なニーズはすべて、ビューアAPI自体でカバーされています。

ただし、高度な使用例では、Webページが`getComponent()`ビューアAPIを使用して内部のSDKコンポーネントを参照し、SDK自体のAPIをすべて柔軟に使用する必要があります。

ビューアでSDKコンポーネントの読み込みと初期化に使用される名前空間は、ビューアの動作環境によって異なります。 ビューアがAdobe Experience Managerで動作している場合、ビューアはSDKコンポーネントを`s7viewers.s7sdk`名前空間に読み込みます。 同様に、Dynamic Media Classicから提供されたビューアがSDKを`s7classic.s7sdk`に読み込みます。

どちらの場合も、ビューア内のSDKで使用される名前空間のプレフィックスは`s7viewers`または`s7classic`です。 また、SDKユーザーガイドまたはSDK APIドキュメントで使用されているプレーンな`s7sdk`名前空間とは異なります。

そのため、内部のビューアコンポーネントと通信するカスタムアプリケーションコードを記述する際には、完全修飾SDK名前空間を使用することが重要です。

例えば、`StatusEvent.NOTF_VIEW_READY`イベントをリッスンする予定で、ビューアがExperience Managerから提供される場合、完全修飾イベントタイプは`s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`で、イベントリスナーのコードは次のようになります。

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
   videoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
