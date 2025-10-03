---
title: Adobe Analyticsのトラッキングのサポート
description: Adobe Analyticsのトラッキングのサポート
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User,Data Engineer,Data Architect
exl-id: 9e321684-4861-4d81-b55c-66c77635930e
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---

# Adobe Analyticsのトラッキングのサポート{#support-for-adobe-analytics-tracking}

## カスタムトラッキング {#section-cda48fc9730142d0bb3326bac7df3271}

デフォルトでは、ビューアは、設定された Image Server に対して、ビューアのタイプとバージョン情報を含む単一のトラッキング HTTP リクエストを送信します。

サードパーティの分析システムと統合するには、`trackEvent` ビューアのコールバックをリッスンし、必要に応じてコールバック関数の `eventInfo` 引数を処理する必要があります。

<!-- The following code is an example of such handler function: -->

<!--

```java {.line-numbers}
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
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

-->

ビューアは、次のSDK ユーザーイベントを追跡します。

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
   <td colname="col1"> <p> <span class="codeph"> BANNER </span> </p> </td> 
   <td colname="col2"> <p>カルーセルバナーの画像が変更されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>ユーザーはホットスポットをアクティベートします。 </p> </td> 
  </tr> 
 </tbody> 
</table>
