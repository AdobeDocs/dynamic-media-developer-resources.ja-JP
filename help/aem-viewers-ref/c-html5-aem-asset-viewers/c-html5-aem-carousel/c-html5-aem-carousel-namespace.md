---
title: ビューア SDK 名前空間
description: ビューア SDK 名前空間
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 1712f08c-70e6-483e-a4e5-614448f35374
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# ビューア SDK 名前空間{#viewer-sdk-namespace}

ビューアは、多くの Viewer SDK コンポーネントで構成されています。 通常、web ページは SDK コンポーネント API を直接操作する必要はありません。一般的なニーズはすべて、ビューア API 自体で説明されています。

ただし、高度なユースケースによっては、web ページで `getComponent()` ビューア API を使用して内部 SDK コンポーネントを参照してから、SDK 自体の API の柔軟性をすべて利用する必要があります。

ビューアによる SDK コンポーネントの読み込みと初期化に使用される名前空間は、ビューアが動作している環境によって異なります。 Adobe Experience Managerでビューアを実行している場合、ビューアは SDK コンポーネントを名前空間 `s7viewers.s7sdk` 読み込みます。 そして、Dynamic Media Classicから提供されるビューアが SDK を `s7classic.s7sdk` に読み込みます。

どちらの場合でも、ビューア内で SDK によって使用される名前空間には、プレフィックスとして `s7viewers` または `s7classic` が付きます。 また、SDK ユーザーガイドや SDK API ドキュメントで使用されるプレーン `s7sdk` 名前空間とは異なります。

そのため、内部ビューアコンポーネントと通信するカスタムアプリケーションコードを記述する場合は、完全修飾された SDK 名前空間を使用することが重要です。

例えば、イベントをリッスンす `StatusEvent.NOTF_VIEW_READY` 予定で、ビューアがExperience Managerから提供される場合、完全修飾イベントタイプは `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` であり、イベントリスナーコードは次のようになります。

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var carouselView = <instance>.getComponent("carouselView"); 
   carouselView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
