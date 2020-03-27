---
description: 'null'
seo-description: 'null'
seo-title: ビューアSDK名前空間
solution: Experience Manager
title: ビューアSDK名前空間
topic: Dynamic media
uuid: e0113556-708c-4898-93f9-b3888de00afc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ビューアSDK名前空間{#viewer-sdk-namespace}

ビューアは、多数のビューアSDKコンポーネントで構築されています。 ほとんどの場合、WebページはSDKコンポーネントAPIと直接やり取りする必要はありません。一般的なニーズはすべて、Viewer API自体で説明されています。

ただし、高度な使用例によっては、WebページがビューアAPIを使用して内部SDKコンポーネントへの参照を取得し、その後SDK自体のAPIの柔軟性をすべて使用する必要があります。 `getComponent()`

ビューアでSDKコンポーネントの読み込みと初期化に使用される名前空間は、ビューアが動作している環境によって異なります。 ビューアがAEM(Adobe Experience Manager)で実行されている場合、ビューアはSDKコンポーネントを名前空間に読み込 `s7viewers.s7sdk` みます。 同様に、Scene7 Publishing Systemから提供されるビューアは、SDKをに読み込みま `s7classic.s7sdk`す。

どちらの場合も、ビューア内のSDKが使用する名前空間には、またはのいずれかのプレフ `s7viewers` ィックス `s7classic` が付けられます。 また、SDKユーザーガイドまたはSDK APIドキュメ `s7sdk` ントで使用されるプレーン名前空間とは異なります。

そのため、内部ビューアコンポーネントと通信するカスタムアプリケーションコードを作成する場合は、完全修飾のSDK名前空間を使用することが重要です。

例えば、イベントをリッスンする予定で、ビューアがAEM `StatusEvent.NOTF_VIEW_READY` から供給される場合、完全修飾イベントタイプはで `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`き、イベントリスナーコードは次のようになります。

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

