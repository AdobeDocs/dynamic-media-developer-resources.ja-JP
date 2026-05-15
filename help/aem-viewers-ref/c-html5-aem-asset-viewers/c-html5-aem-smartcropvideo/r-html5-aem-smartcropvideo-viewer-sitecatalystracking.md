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
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 177
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
