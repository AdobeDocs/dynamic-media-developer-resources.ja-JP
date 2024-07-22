---
title: Adobe Analyticsのトラッキングのサポート
description: 混在メディアビューアでは、Adobe Analyticsのトラッキングをすぐに使用できます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User,Data Engineer,Data Architect
exl-id: 3b28c853-3747-4805-a141-3cce1398d783
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# Adobe Analyticsのトラッキングのサポート{#support-for-adobe-analytics-tracking}

混在メディアビューアでは、Adobe Analyticsのトラッキングをすぐに使用できます。

## 標準のトラッキング {#section-ba994f079d0343c8ae48adffaa3195a3}

混在メディアビューアでは [!DNL Adobe Analytics] 標準のトラッキングがサポートされています。 トラッキングを有効にするには、適切な会社プリセット名 `config2` パラメーターとして渡します。

また、ビューアは、1 つのトラッキング HTTP リクエストを、ビューアのタイプとバージョン情報と共に、設定済みの Image Server に送信します。

## カスタムトラッキング {#section-cda48fc9730142d0bb3326bac7df3271}

サードパーティの分析システムと統合するには、`trackEvent` ビューアのコールバックをリッスンし、必要に応じてコールバック関数の `eventInfo` 引数を処理する必要があります。 次のコードは、このようなハンドラー関数の例です。

```javascript {.line-numbers}
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
   <td colname="col2"> <p>setAsset （） </span> API を使用して、ビューア内 <span class="codeph"> アセットが入れ替えられます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p>画像がズームされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>画像がパンされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWATCH </span> </p> </td> 
   <td colname="col2"> <p> 画像を変更するには、スウォッチをクリックまたはタップします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>再生が開始されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>再生が一時停止した。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>再生が停止した。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マイルストーン </span> </p> </td> 
   <td colname="col2"> <p>再生が次のマイルストーンのいずれかに達します：0%、25%、50%、75%、100%。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SPIN </span> </p> </td> 
   <td colname="col2"> <p>スピンが実行されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>
