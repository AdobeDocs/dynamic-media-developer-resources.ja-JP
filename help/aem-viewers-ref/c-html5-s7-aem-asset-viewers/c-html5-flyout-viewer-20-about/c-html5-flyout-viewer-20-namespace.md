---
description: ビューアSDKの名前空間
solution: Experience Manager
title: ビューアSDKの名前空間
topic: Dynamic media
uuid: 5fa7102b-c93d-4865-9e14-fa8813403de2
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---


# ビューアSDK名前空間{#viewer-sdk-namespace}

ビューアは、多数のビューアSDKコンポーネントで構築されています。 ほとんどの場合、Webページは、SDKコンポーネントAPIと直接やり取りする必要はありません。一般的なニーズはすべて、ビューアのAPI自体で扱われています。

ただし、高度な使用例によっては、Webページが`getComponent()`ビューアAPIを使用して内部SDKコンポーネントへの参照を取得し、SDK自体のAPIを柔軟に使用する必要があります。

ビューアでSDKコンポーネントの読み込みと初期化に使用される名前空間は、ビューアが動作している環境によって異なります。 ビューアがAEM(Adobe Experience Manager)で実行されている場合、ビューアはSDKコンポーネントを`s7viewers.s7sdk`名前空間に読み込みます。 同様に、Scene7パブリッシングシステムから提供されるビューアは、SDKを`s7classic.s7sdk`に読み込みます。

どちらの場合も、ビューア内のSDKが使用する名前空間のプレフィックスは`s7viewers`または`s7classic`です。 また、SDKユーザーガイドまたはSDK APIドキュメントで使用されている通常の`s7sdk`名前空間とは異なります。 そのため、内部ビューアコンポーネントと通信するカスタムアプリケーションコードを作成する場合は、完全修飾されたSDK名前空間を使用することが重要です。

例えば、`StatusEvent.NOTF_VIEW_READY`イベントをリッスンする予定で、ビューアがAEMから供給される場合、完全修飾イベントタイプは`s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`で、イベントリスナーコードは次のようになります。

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Scene7 SPS will look like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```

