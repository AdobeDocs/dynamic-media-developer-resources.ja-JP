---
description: スピンビューアでは、Adobe Analytics追跡機能がサポートされていて、この機能をすぐに使用できます。
seo-description: スピンビューアでは、Adobe Analytics追跡機能がサポートされていて、この機能をすぐに使用できます。
seo-title: Adobe Analyticsトラッキングのサポート
solution: Experience Manager
title: Adobe Analyticsトラッキングのサポート
topic: Dynamic media
uuid: 337671f0-22e8-4e3e-a0a9-ce49d271ea56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---


# Adobe Analyticsトラッキングのサポート{#support-for-adobe-analytics-tracking}

スピンビューアでは、Adobe Analytics追跡機能がサポートされていて、この機能をすぐに使用できます。

## すぐに使える追跡{#section-d06145cfa2b9491bb485b599368d466e}

スピンビューアでは、Adobe Analyticsの追跡機能がサポートされていて、この機能をすぐに使用できます。

追跡を有効にするには、適切な会社プリセット名を`config2`パラメーターとして渡します。

また、ビューアは、設定済みのImage Serverに、ビューアのタイプとバージョン情報と共に、1つの追跡HTTP要求を送信します。

## カスタムトラッキング{#section-47512156a1d64b338b50cfa39c84f4aa}

サードパーティの分析システムと統合するには、`trackEvent`ビューアコールバックをリッスンし、必要に応じてコールバック関数の`eventInfo`引数を処理する必要があります。 次のコードは、このようなハンドラー関数の例です。

```
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
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
   <td colname="col1"> <p> <span class="codeph"> SPIN </span> </p> </td> 
   <td colname="col2"> <p> スピンが実行された。 </p> </td> 
  </tr> 
 </tbody> 
</table>

