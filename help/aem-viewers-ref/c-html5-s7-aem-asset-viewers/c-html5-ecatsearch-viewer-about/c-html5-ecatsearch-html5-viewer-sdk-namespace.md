---
description: ビューア SDK名前空間
solution: Experience Manager
title: ビューア SDK名前空間
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: aaad8f43-f6f2-440f-a6c4-52db585b48da
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# ビューア SDK名前空間{#viewer-sdk-namespace}

ビューアは、多くのビューア SDK コンポーネントで構成されています。 ほとんどの場合、web ページはSDK コンポーネント API を直接操作する必要はありません。一般的なニーズはすべて、ビューア API 自体で説明されています。

ただし、高度なユースケースによっては、web ページで `getComponent()` ビューア API を使用して内部SDK コンポーネントへの参照を取得し、SDK自体の API の柔軟性をすべて利用する必要があります。

ビューアによるSDK コンポーネントの読み込みと初期化に使用される名前空間は、ビューアが動作している環境によって異なります。 ビューアがAEM（Adobe Experience Manager）で動作している場合、ビューアはSDK コンポーネントを名前空間に読み込 `s7viewers.s7sdk` ます。 Dynamic Media Classicから提供されるビューアが、SDKを `s7classic.s7sdk` に読み込みます。

どちらの場合も、ビューア内のSDKで使用される名前空間には、プレフィックスとして `s7viewers` または `s7classic` が付きます。 また、SDK ユーザーガイドやSDK API ドキュメントで使用されているプレーン `s7sdk` 名前空間とは異なります。

そのため、内部ビューアコンポーネントと通信するカスタムアプリケーションコードを記述する場合は、完全修飾されたSDK名前空間を使用することが重要です。

例えば、イベントをリッスンす `StatusEvent.NOTF_VIEW_READY` 予定で、ビューアがDynamic Media Classicから提供される場合、完全修飾イベントタイプは `s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY` であり、イベントリスナーコードは次のようになります。

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var pageView = <instance>.getComponent("pageView"); 
   pageView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
