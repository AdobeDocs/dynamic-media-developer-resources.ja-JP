---
description: Adobe Analyticsトラッキングのサポート
solution: Experience Manager
title: Adobe Analyticsトラッキングのサポート
uuid: a7de5549-2a9d-4153-be5e-72705ced85ac
feature: Dynamic Mediaクラシック，ビューア，SDK/API，カルーセルバナー
role: 開発者，業者，データエンジニア，データアーキテクト
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 1%

---


# Adobe Analyticsトラッキングのサポート{#support-for-adobe-analytics-tracking}

## カスタムトラッキング{#section-cda48fc9730142d0bb3326bac7df3271}

初期設定では、ビューアは、ビューアタイプとバージョン情報を含む設定済みのImage Serverに、1つの追跡HTTP要求を送信します。

サードパーティの分析システムと統合するには、`trackEvent`ビューアコールバックをリッスンし、必要に応じてコールバック関数の`eventInfo`引数を処理する必要があります。 次のコードは、このようなハンドラー関数の例です。

```
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
   <td colname="col2"> <p>ビューアが最初に読み込まれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> バナー  </span> </p> </td> 
   <td colname="col2"> <p>カルーセルバナーの画像が変更されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>ユーザーがホットスポットをアクティブにします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

