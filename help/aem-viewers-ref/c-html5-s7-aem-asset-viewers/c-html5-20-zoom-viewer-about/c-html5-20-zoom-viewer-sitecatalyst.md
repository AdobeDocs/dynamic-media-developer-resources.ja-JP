---
title: Adobe Analyticsのトラッキングのサポート
description: Adobe Analyticsのトラッキングのサポート
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User,Data Engineer,Data Architect
exl-id: 5f927a4b-b9c8-4750-9d1c-c252d87fd236
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# Adobe Analyticsのトラッキングのサポート{#support-for-adobe-analytics-tracking}

## 標準のトラッキング {#section-ba994f079d0343c8ae48adffaa3195a3}

ビデオビューアは [!DNL Adobe Analytics] 標準のトラッキングをサポートしています。 トラッキングを有効にするには、適切な会社プリセット名 `config2` パラメーターとして渡します。

また、ビューアは、1 つのトラッキング HTTP リクエストを、ビューアのタイプとバージョン情報と共に、設定済みの Image Server に送信します。

## カスタムトラッキング {#section-cda48fc9730142d0bb3326bac7df3271}

サードパーティの分析システムと統合するには、`trackEvent` ビューアのコールバックをリッスンし、必要に応じてコールバック関数の `eventInfo` 引数を処理する必要があります。 次のコードは、このようなハンドラー関数の例です。

```javascript {.line-numbers}
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

ビューアは、次の SDK ユーザーイベントを追跡します。

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
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> setAsset （） </span> API を使用して、ビューア内でアセットがスワップされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p> 画像がズームされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>画像がパンされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWATCH </span> </p> </td> 
   <td colname="col2"> <p> 画像を変更するには、スウォッチをクリックまたはタップします。 </p> </td> 
  </tr> 
 </tbody> 
</table>
