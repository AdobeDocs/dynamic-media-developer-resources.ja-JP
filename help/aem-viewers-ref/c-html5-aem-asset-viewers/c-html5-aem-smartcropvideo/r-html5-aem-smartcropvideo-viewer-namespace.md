---
title: Viewer SDK名前空間
description: Viewer SDK名前空間
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 6cbf7eef-0d17-4411-9a74-22455009f66d
TQID: 'https://experienceleague.adobe.com/jP-ctDVghPscHD19iQPa4s5GnTyXKIIFOFu4UJTFo98'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '220'
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
  var smartCropVideoPlayer = <instance>.getComponent("smartCropVideoPlayer"); 
   smartCropVideoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for the viewer served from Dynamic Media Classic looks like the following: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var smartCropVideoPlayer = <instance>.getComponent("smartCropVideoPlayer"); 
   smartCropVideoPlayer.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
