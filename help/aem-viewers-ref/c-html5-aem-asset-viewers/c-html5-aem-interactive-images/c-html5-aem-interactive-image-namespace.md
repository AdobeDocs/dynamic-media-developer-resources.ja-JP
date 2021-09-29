---
title: ビューア SDK の名前空間
description: ビューア SDK の名前空間
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 8e37bb60-c875-48d6-8c86-93aba7f50f74
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# ビューア SDK の名前空間{#viewer-sdk-namespace}

このビューアは、多くのビューア SDK コンポーネントで構築されています。 通常、Web ページは、SDK コンポーネント API を直接操作する必要はありません。一般的なニーズはすべて、ビューア API 自体でカバーされています。

ただし、高度な使用例の中には、 `getComponent()` ビューア API を使用して Web ページが内部の SDK コンポーネントを参照し、SDK 自体の API をすべて柔軟に使用する必要があるものもあります。

ビューアで SDK コンポーネントの読み込みと初期化に使用される名前空間は、ビューアの動作環境によって異なります。 ビューアがAdobe Experience Managerで実行されている場合、ビューアは SDK コンポーネントを `s7viewers.s7sdk` 名前空間に読み込みます。 また、Dynamic Media Classic から提供されたビューアが、SDK を `s7classic.s7sdk` に読み込みます。

どちらの場合も、ビューア内の SDK で使用される名前空間のプレフィックスは `s7viewers` または `s7classic` です。 また、SDK ユーザーガイドまたは SDK API ドキュメントで使用されているプレーンな `s7sdk` 名前空間とは異なります。

そのため、内部のビューアコンポーネントと通信するカスタムアプリケーションコードを記述する際には、完全修飾された SDK 名前空間を使用することが重要です。

例えば、`StatusEvent.NOTF_VIEW_READY` イベントをリッスンし、ビューアをExperience Managerから提供する場合、完全修飾イベントタイプは `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` で、イベントリスナーコードは次のようになります。

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
