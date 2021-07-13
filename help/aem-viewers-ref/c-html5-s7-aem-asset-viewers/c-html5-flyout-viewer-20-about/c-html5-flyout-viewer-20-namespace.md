---
description: ビューアSDKの名前空間
solution: Experience Manager
title: ビューアSDKの名前空間
feature: Dynamic Media Classic，ビューア，SDK/API，フライアウト
role: Developer,User
exl-id: 06a7110a-3a6f-42f9-b729-e8f96762c64e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---

# ビューアSDKの名前空間{#viewer-sdk-namespace}

このビューアは、多くのビューアSDKコンポーネントで構築されています。 ほとんどの場合、WebページはSDKコンポーネントAPIを直接操作する必要はありません。一般的なニーズはすべて、ビューアAPI自体でカバーされています。

ただし、高度な使用例では、Webページが`getComponent()`ビューアAPIを使用して内部のSDKコンポーネントへの参照を取得し、SDK自体のAPIをすべて柔軟に使用する必要があります。

ビューアでSDKコンポーネントの読み込みと初期化に使用される名前空間は、ビューアの動作環境によって異なります。 ビューアがAEM(Adobe Experience Manager)で実行されている場合、ビューアはSDKコンポーネントを`s7viewers.s7sdk`名前空間に読み込みます。 同様に、Dynamic Media Classicから提供されたビューアがSDKを`s7classic.s7sdk`に読み込みます。

どちらの場合も、ビューア内のSDKで使用される名前空間のプレフィックスは`s7viewers`または`s7classic`です。 また、SDKユーザーガイドまたはSDK APIドキュメントで使用されているプレーンな`s7sdk`名前空間とは異なります。 そのため、内部のビューアコンポーネントと通信するカスタムアプリケーションコードを記述する際には、完全修飾SDK名前空間を使用することが重要です。

例えば、`StatusEvent.NOTF_VIEW_READY`イベントをリッスンする予定で、ビューアがAEMから提供される場合、完全修飾イベントタイプは`s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`で、イベントリスナーのコードは次のようになります。

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Dynamic Media Classic will look like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
