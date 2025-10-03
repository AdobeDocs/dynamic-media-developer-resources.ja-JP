---
title: Adobe Analyticsのトラッキングのサポート
description: HTML5 Video360 ビューアでは、Adobe Analyticsのトラッキングをすぐに使用できます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User,Data Engineer,Data Architect
exl-id: 74a69d01-fa58-4d36-8598-992baf6ae11d
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# Adobe Analyticsのトラッキングのサポート{#support-for-adobe-analytics-tracking}

HTML5 Video360 ビューアでは、Adobe Analyticsのトラッキングをすぐに使用できます。

トラッキングを有効にするには、適切な会社プリセット名 `config2` パラメーターとして渡します。

デフォルトでは、ビューアは、設定された Image Server にビューアのタイプとバージョン情報を含む単一のトラッキング HTTP リクエストを送信します。

## カスタムトラッキング {#section-cda48fc9730142d0bb3326bac7df3271}

サードパーティの分析システムと統合するには、`trackEvent` ビューアのコールバックをリッスンし、必要に応じてコールバック関数の `eventInfo` 引数を処理する必要があります。


次のコードは、このようなハンドラー関数の例です。

```javascript {.line-numbers}
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
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


ビューアは、次のSDK ユーザーイベントを追跡します。

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK ユーザーイベント </p> </th> 
   <th colname="col2" class="entry"> <p>送信済み… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>ビューアが最初に読み込まれるとき。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>setAsset （） <span class="codeph"> API を使用してビューアでアセット </span> スワップした場合。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>再生の開始時。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>再生が一時停止したとき。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>再生が停止したとき。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マイルストーン </span> </p> </td> 
   <td colname="col2"> <p>再生が 0%、25%、50%、75%、100% のいずれかのマイルストーンに達した場合。 </p> </td> 
  </tr> 
 </tbody> 
</table>
