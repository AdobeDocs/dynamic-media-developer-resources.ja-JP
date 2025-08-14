---
title: ビューア SDK名前空間
description: ビューア SDK名前空間
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: d1f12c9d-9b00-44ee-bd91-76a4d882fecf
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# ビューア SDK名前空間{#viewer-sdk-namespace}

ビューアは、多くのビューア SDK コンポーネントで構成されています。 通常、web ページはSDK コンポーネント API を直接操作する必要はありません。一般的なニーズはすべて、ビューア API 自体で説明されています。

ただし、高度なユースケースによっては、web ページで `getComponent()` ビューア API を使用して内部のSDK コンポーネントを参照してから、SDK自体の API の柔軟性をすべて利用する必要があります。

ビューアによるSDK コンポーネントの読み込みと初期化に使用される名前空間は、ビューアが動作している環境によって異なります。 Adobe Experience Managerでビューアを実行している場合、ビューアはSDK コンポーネントを名前空間に読み込 `s7viewers.s7sdk` ます。 同様に、Dynamic Media Classicから提供されるビューアは、SDKを `s7classic.s7sdk` に読み込みます。

どちらの場合も、ビューア内のSDKで使用される名前空間には、プレフィックスとして `s7viewers` または `s7classic` が付きます。 また、SDK ユーザーガイドやSDK API ドキュメントで使用されているプレーン `s7sdk` 名前空間とは異なります。 そのため、内部のビューアコンポーネントと通信するカスタムアプリケーションコードを記述する場合は、完全修飾されたSDK名前空間を使用することが重要です。

例えば、イベントをリッスンす `StatusEvent.NOTF_VIEW_READY` 予定で、ビューアがExperience Managerから提供される場合、完全修飾イベントタイプは `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` であり、イベントリスナーコードは次のようになります。

```javascript {.line-numbers}
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
