---
title: Adobe Analytics トラッキングのサポート
description: スマート切り抜きビデオビューアは、Adobe Analyticsのトラッキングをすぐにサポートします。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 0d91ca94-79fc-40de-8095-0252688ebe76
TQID: 'https://experienceleague.adobe.com/qxJCNOQ6B6iYDi7JRepZfc9gMaF4Wn50DoPYWnTsq5Y'
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
source-wordcount: '177'
ht-degree: 0%
---
# Adobe Analytics トラッキングのサポート{#support-for-adobe-analytics-tracking}

スマート切り抜きビデオビューアは、Adobe Analyticsのトラッキングをすぐにサポートします。

## すぐに利用できるトラッキング機能 {#section-3b101fe30be943c1b679fd5c273569ca}

スマート切り抜きビデオビューアは、Adobe Analyticsのトラッキングをすぐにサポートします。

トラッキングを有効にするには、適切な会社プリセット名を`config2` パラメーターとして渡します。

ビューアは、ビューアのタイプとバージョン情報を使用して、設定されたImage Serverに1つのトラッキング HTTP リクエストを送信します。

## カスタムトラッキング {#section-ab10bd7caf184721a366cf3953071934}

サードパーティの分析システムと統合するには、`trackEvent` ビューアのコールバックをリッスンし、必要に応じてコールバック関数の`eventInfo`引数を処理する必要があります。 以下のコードは、そのようなハンドラー関数の例です。

```javascript {.line-numbers}
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
}, 
"handlers":{ 
 "trackEvent":function(objID, compClass, instName, timeStamp, eventInfo) { 
  //identify event type 
  var eventType = eventInfo.split(",")[0]; 
  switch (eventType) { 
   case "LOAD": 
    //custom event processing code 
    break; 
   //additional cases for other events 
} 
} 
} 
});
```

ビューアは、次のSDK ユーザーイベントをトラッキングします。

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK ユーザーイベント </p> </th> 
   <th colname="col2" class="entry"> <p>送信日時… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">を読み込み</span> </p> </td> 
   <td colname="col2"> <p>ビューアが最初に読み込まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> スワップ </span> </p> </td> 
   <td colname="col2"> <p>アセットは、<span class="codeph"> setAsset （） </span> APIを使用してビューアでスワップされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span>を再生 </p> </td> 
   <td colname="col2"> <p>再生が開始されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">一時停止</span> </p> </td> 
   <td colname="col2"> <p>再生が一時停止しています。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">分岐点</span> </p> </td> 
   <td colname="col2"> <p>再生が停止しています。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マイルストーン </span> </p> </td> 
   <td colname="col2"> <p>再生は、0%、25%、50%、75%、100%のいずれかのミルストーンに達します。 </p> </td> 
  </tr> 
 </tbody> 
</table>
