---
description: 分析トラッキングのサポート
solution: Experience Manager
title: 分析トラッキングのサポート
feature: Dynamic Media Classic，ビューア，SDK/API，インタラクティブ画像
role: Developer,Business Practitioner,Data Engineer,Data Architect
exl-id: 17e8937f-e328-46a4-b7d9-1fd39ab2e8bd
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 2%

---

# 分析トラッキングのサポート{#support-for-analytics-tracking}

## カスタムトラッキング {#section-cda48fc9730142d0bb3326bac7df3271}

デフォルトでは、ビューアは、設定済みのImage Serverに対し、ビューアのタイプとバージョン情報を含む単一の追跡HTTP要求を送信します。

サードパーティの分析システムと統合するには、 `trackEvent`ビューアコールバックをリッスンし、必要に応じてコールバック関数の`eventInfo`引数を処理する必要があります。 次のコードは、このようなハンドラー関数の例です。

```
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
  "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
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

ビューアは、次のSDKユーザーイベントを追跡します。

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDKユーザーイベント </p> </th> 
   <th colname="col2" class="entry"> <p>送信タイミング… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>ビューアが最初に読み込まれたとき。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>ユーザーはホットスポットをアクティブにします。 </p> </td> 
  </tr> 
 </tbody> 
</table>
