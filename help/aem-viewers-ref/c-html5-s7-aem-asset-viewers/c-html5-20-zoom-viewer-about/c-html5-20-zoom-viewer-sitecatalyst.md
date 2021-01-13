---
description: Adobe Analyticsトラッキングのサポート
solution: Experience Manager
title: Adobe Analyticsトラッキングのサポート
topic: Dynamic media
uuid: d5399638-3fc5-4f95-841d-5c6d4d35bda2
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 3%

---


# Adobe Analyticsトラッキングのサポート{#support-for-adobe-analytics-tracking}

## すぐに使える追跡{#section-ba994f079d0343c8ae48adffaa3195a3}

ビデオビューアでは、[!DNL Adobe Analytics]追跡機能がサポートされていて、この機能をすぐに使用できます。 追跡を有効にするには、適切な会社プリセット名を`config2`パラメーターとして渡します。

また、ビューアは、設定済みのImage Serverに、ビューアのタイプとバージョン情報と共に、1つの追跡HTTP要求を送信します。

## カスタムトラッキング{#section-cda48fc9730142d0bb3326bac7df3271}

サードパーティの分析システムと統合するには、`trackEvent`ビューアコールバックをリッスンし、必要に応じてコールバック関数の`eventInfo`引数を処理する必要があります。 次のコードは、このようなハンドラー関数の例です。

```
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
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
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p> 画像がズームされたとき。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>画像がパンされた。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWATCH </span> </p> </td> 
   <td colname="col2"> <p> スウォッチをクリックまたはタップして画像が変更された。 </p> </td> 
  </tr> 
 </tbody> 
</table>

