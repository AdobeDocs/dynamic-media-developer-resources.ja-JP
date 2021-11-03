---
title: Adobe Analytics追跡のサポート
description: スマート切り抜きビデオビューアでは、Adobe Analyticsの追跡機能がサポートされていて、この機能をすぐに使用できます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User,Data Engineer,Data Architect
exl-id: 2cc7087d-ed02-4560-b9ce-533af2b11a24
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# Adobe Analytics追跡のサポート{#support-for-adobe-analytics-tracking}

スマート切り抜きビデオビューアでは、Adobe Analyticsの追跡機能がサポートされていて、この機能をすぐに使用できます。

## 標準の追跡 {#section-3b101fe30be943c1b679fd5c273569ca}

スマート切り抜きビデオビューアでは、Adobe Analyticsの追跡機能がサポートされていて、この機能をすぐに使用できます。

追跡を有効にするには、適切な会社プリセット名を `config2` パラメーター。

また、ビューアのタイプとバージョン情報と共に、設定済みの Image Server に 1 つの追跡 HTTP 要求が送信されます。

## カスタムトラッキング {#section-ab10bd7caf184721a366cf3953071934}

をサードパーティの分析システムと統合するには、 `trackEvent` ビューアのコールバックとプロセス `eventInfo` 必要に応じて、コールバック関数の引数です。 次のコードは、このようなハンドラー関数の例です。

```
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

ビューアは、次の SDK ユーザーイベントを追跡します。

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK ユーザーイベント </p> </th> 
   <th colname="col2" class="entry"> <p>次の場合に送信… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>ビューアが最初に読み込まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>ビューアで <span class="codeph"> setAsset() </span> API </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>再生が開始されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>再生が一時停止された。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>再生が停止しました。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>再生が次の 1 つのミリストーンに達しました。0%、25%、50%、75%、100%です。 </p> </td> 
  </tr> 
 </tbody> 
</table>
