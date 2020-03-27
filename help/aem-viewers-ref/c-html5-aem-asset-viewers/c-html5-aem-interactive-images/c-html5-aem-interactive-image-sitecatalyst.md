---
description: 'null'
seo-description: 'null'
seo-title: 解析追跡のサポート
solution: Experience Manager
title: 解析追跡のサポート
topic: Dynamic media
uuid: ae870d2e-2a09-4551-935a-916d0e657653
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 解析追跡のサポート{#support-for-analytics-tracking}

## カスタム追跡 {#section-cda48fc9730142d0bb3326bac7df3271}

初期設定では、ビューアは、ビューアのタイプとバージョン情報を含む単一の追跡HTTP要求を設定済みのImage Serverに送信します。

サードパーティの分析システムと統合するには、ビューアのコールバックをリッスンし、必要に応じ `trackEvent` てコールバック関数の `eventInfo` 引数を処理する必要があります。 次のコードは、このようなハンドラー関数の例です。

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
   <th colname="col2" class="entry"> <p>送信日時… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>ビューアが最初に読み込まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>ユーザーがホットスポットをアクティブにします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

