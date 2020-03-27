---
description: 混在メディアビューアでは、Adobe Analyticsの追跡機能がサポートされていて、この機能をすぐに使用できます。
seo-description: 混在メディアビューアでは、Adobe Analyticsの追跡機能がサポートされていて、この機能をすぐに使用できます。
seo-title: Adobe Analyticsの追跡のサポート
solution: Experience Manager
title: Adobe Analyticsの追跡のサポート
topic: Dynamic media
uuid: ad4dfed6-121f-4adb-bbdb-db6e6ee5672d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Adobe Analyticsの追跡のサポート{#support-for-adobe-analytics-tracking}

混在メディアビューアでは、Adobe Analyticsの追跡機能がサポートされていて、この機能をすぐに使用できます。

## 追跡機能をすぐに使用できる機能 {#section-ba994f079d0343c8ae48adffaa3195a3}

混在メディアビューアでは、追 [!DNL Adobe Analytics] 跡機能がサポートされていて、この機能をすぐに使用できます。 追跡を有効にするには、適切な会社プリセット名をパラメーターとして渡 `config2` します。

また、ビューアは、設定済みのImage Serverに対して、ビューアのタイプとバージョン情報と共に単一の追跡HTTP要求を送信します。

## カスタム追跡 {#section-cda48fc9730142d0bb3326bac7df3271}

サードパーティの分析システムと統合するには、ビューアのコールバックをリッスンし、必要に応じ `trackEvent` てコールバック関数の `eventInfo` 引数を処理する必要があります。 次のコードは、このようなハンドラー関数の例です。

```
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
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
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>setAsset() <span class="codeph"></span> APIを使用して、ビューア内でアセットが入れ替わった場合。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p>画像がズームされた。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>画像がパンされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWATCH </span> </p> </td> 
   <td colname="col2"> <p> スウォッチをクリックまたはタップすると、画像が変更されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>再生が開始された。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>再生が一時停止された。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>再生が停止した。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>再生が次のいずれかのマイルストーンに達しました。0%、25%、50%、75%、100%。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SPIN </span> </p> </td> 
   <td colname="col2"> <p>スピンが実行されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

