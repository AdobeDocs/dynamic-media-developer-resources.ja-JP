---
title: Adobe Analyticsのトラッキングのサポート
description: スマート切り抜きビデオビューアでは、すぐに使用できるAdobe Analytics トラッキングがサポートされています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User,Data Engineer,Data Architect
exl-id: 0d91ca94-79fc-40de-8095-0252688ebe76
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# Adobe Analyticsのトラッキングのサポート{#support-for-adobe-analytics-tracking}

スマート切り抜きビデオビューアでは、すぐに使用できるAdobe Analytics トラッキングがサポートされています。

## 標準のトラッキング {#section-3b101fe30be943c1b679fd5c273569ca}

スマート切り抜きビデオビューアでは、すぐに使用できるAdobe Analytics トラッキングがサポートされています。

トラッキングを有効にするには、適切な会社プリセット名 `config2` パラメーターとして渡します。

また、ビューアは、1 つのトラッキング HTTP リクエストを、ビューアのタイプとバージョン情報と共に、設定済みの Image Server に送信します。

## カスタムトラッキング {#section-ab10bd7caf184721a366cf3953071934}

サードパーティの分析システムと統合するには、ビューアのコールバック `trackEvent` リッスンし、必要に応じてコールバック関数の引数 `eventInfo` 処理する必要があります。 次のコードは、このようなハンドラー関数の例です。

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
   <td colname="col2"> <p>setAsset （） </span> API を使用して、ビューア内 <span class="codeph"> アセットが入れ替えられます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>再生が開始されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>再生が一時停止した。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>再生が停止した。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マイルストーン </span> </p> </td> 
   <td colname="col2"> <p>再生が次のマイルストーンのいずれかに達します：0%、25%、50%、75%、100%。 </p> </td> 
  </tr> 
 </tbody> 
</table>
