---
description: ビデオビューアでは、Adobe Analyticsの追跡機能がサポートされていて、この機能をすぐに使用できます。
seo-description: ビデオビューアでは、Adobe Analyticsの追跡機能がサポートされていて、この機能をすぐに使用できます。
seo-title: Adobe Analyticsトラッキングのサポート
solution: Experience Manager
title: Adobe Analyticsトラッキングのサポート
topic: Dynamic media
uuid: c53b3d3b-42e5-4c87-8a1e-87c73eb32341
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 3%

---


# Adobe Analyticsトラッキングのサポート{#support-for-adobe-analytics-tracking}

ビデオビューアでは、Adobe Analyticsの追跡機能がサポートされていて、この機能をすぐに使用できます。

## すぐに使える追跡{#section-3b101fe30be943c1b679fd5c273569ca}

ビデオビューアでは、Adobe Analyticsの追跡機能がサポートされていて、この機能をすぐに使用できます。

追跡を有効にするには、適切な会社プリセット名を`config2`パラメーターとして渡します。

また、ビューアは、設定済みのImage Serverに、ビューアのタイプとバージョン情報と共に、1つの追跡HTTP要求を送信します。

## カスタムトラッキング{#section-ab10bd7caf184721a366cf3953071934}

サードパーティの分析システムと統合するには、`trackEvent`ビューアコールバックをリッスンし、必要に応じてコールバック関数の`eventInfo`引数を処理する必要があります。 次のコードは、このようなハンドラー関数の例です。

```
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
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

ビューアは、以下のSDKユーザーイベントを追跡します。

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDKのユーザーイベント </p> </th> 
   <th colname="col2" class="entry"> <p>送信日時 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>ビューアが最初に読み込まれたとき。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> setAsset() </span> APIを使用して、ビューア内でアセットが入れ替わったとき。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>再生が開始された。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>再生が次のマイルストーンのいずれかに達した。0%、25%、50%、75%、100%です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

