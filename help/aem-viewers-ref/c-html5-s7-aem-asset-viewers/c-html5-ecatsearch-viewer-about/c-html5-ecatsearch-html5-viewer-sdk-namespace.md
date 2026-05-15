---
description: Viewer SDK名前空間
solution: Experience Manager
title: Viewer SDK名前空間
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: aaad8f43-f6f2-440f-a6c4-52db585b48da
TQID: 'https://experienceleague.adobe.com/wS6VG2Eo73QO7-kbRLVCZ-DOrSWUb6XOB92J-zP7QV8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 227
ht-degree: 0%

---

# Viewer SDK名前空間{#viewer-sdk-namespace}

ビューアは、多くのViewer SDK コンポーネントで構築されています。 ほとんどの場合、web ページはSDK コンポーネント APIと直接やり取りする必要がありません。一般的なニーズはすべてビューア API自体でカバーされています。

ただし、一部の高度なユースケースでは、web ページで`getComponent()` ビューア APIを使用して内部SDK コンポーネントへの参照を取得し、SDK自体のAPIのすべての柔軟性を使用する必要があります。

ビューアによるSDK コンポーネントの読み込みと初期化に使用される名前空間は、ビューアが動作している環境によって異なります。 ビューアがAEM （Adobe Experience Manager）で実行されている場合、ビューアはSDK コンポーネントを`s7viewers.s7sdk`名前空間に読み込みます。 Dynamic Media Classicから提供されたビューアーは、SDKを`s7classic.s7sdk`に読み込みます。

いずれの場合も、ビューア内のSDKで使用される名前空間には、接頭辞として`s7viewers`または`s7classic`が含まれています。 また、SDK ユーザーガイドまたはSDK API ドキュメントで使用されているプレーン `s7sdk`名前空間とは異なります。

そのため、内部ビューアコンポーネントと通信するカスタムアプリケーションコードを記述する場合は、完全修飾SDK名前空間を使用することが重要です。

例えば、`StatusEvent.NOTF_VIEW_READY` イベントをリッスンする予定で、ビューアがDynamic Media Classicから提供される場合、完全修飾イベントの種類は`s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY`であり、イベントリスナーコードは次のようになります。

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
