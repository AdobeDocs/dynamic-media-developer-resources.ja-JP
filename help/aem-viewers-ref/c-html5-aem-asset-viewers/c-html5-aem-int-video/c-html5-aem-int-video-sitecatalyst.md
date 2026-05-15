---
title: Adobe Analytics トラッキングのサポート
description: HTML5 Video360 Viewerは、Adobe Analytics トラッキングをすぐにサポートします。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 74a69d01-fa58-4d36-8598-992baf6ae11d
TQID: 'https://experienceleague.adobe.com/2sgSYMdQRxtNOivwpaNfclocNxH-0HmY26t74wCWPYU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 164
ht-degree: 0%

---

# Adobe Analytics トラッキングのサポート{#support-for-adobe-analytics-tracking}

HTML5 Video360 Viewerは、Adobe Analytics トラッキングをすぐにサポートします。

トラッキングを有効にするには、適切な会社プリセット名を`config2` パラメーターとして渡します。

デフォルトでは、ビューアは、ビューアのタイプとバージョン情報を使用して、設定されたImage Serverに1つのトラッキング HTTP リクエストを送信します。

## カスタムトラッキング {#section-cda48fc9730142d0bb3326bac7df3271}

サードパーティの分析システムと統合するには、`trackEvent` ビューアのコールバックをリッスンし、必要に応じてコールバック関数の`eventInfo`引数を処理する必要があります。


以下のコードは、そのようなハンドラー関数の例です。

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


ビューアは、次のSDK ユーザーイベントをトラッキングします。

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK ユーザーイベント </p> </th> 
   <th colname="col2" class="entry"> <p>送信済… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">を読み込み</span> </p> </td> 
   <td colname="col2"> <p>ビューアが最初に読み込まれるとき。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> スワップ </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> setAsset （） </span> APIを使用してビューアでアセットをスワップすると。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span>を再生 </p> </td> 
   <td colname="col2"> <p>アニメーションが表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">一時停止</span> </p> </td> 
   <td colname="col2"> <p>再生が一時停止されたとき。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">分岐点</span> </p> </td> 
   <td colname="col2"> <p>再生が停止されたとき。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マイルストーン </span> </p> </td> 
   <td colname="col2"> <p>再生が0%、25%、50%、75%、100%のいずれかのマイルストーンに達した場合。 </p> </td> 
  </tr> 
 </tbody> 
</table>
