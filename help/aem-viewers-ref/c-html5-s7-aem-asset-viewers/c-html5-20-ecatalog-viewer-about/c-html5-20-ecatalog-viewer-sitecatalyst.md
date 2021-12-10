---
title: Adobe Analytics追跡のサポート
description: eCatalog ビューアでは、Adobe Analyticsの追跡機能がサポートされていて、この機能をすぐに使用できます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User,Data Engineer,Data Architect
exl-id: 714e8001-06dc-49b1-838f-ab9772f2527c
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Adobe Analytics追跡のサポート{#support-for-adobe-analytics-tracking}

eCatalog ビューアでは、Adobe Analyticsの追跡機能がサポートされていて、この機能をすぐに使用できます。

## 標準の追跡 {#section-ba994f079d0343c8ae48adffaa3195a3}

eCatalog ビューアは、 [!DNL Adobe Analytics] 追跡機能が標準で用意されています。 追跡を有効にするには、適切な会社プリセット名を `config2` パラメーター。

また、ビューアのタイプとバージョン情報と共に、設定済みの Image Server に 1 つの追跡 HTTP 要求が送信されます。

## カスタムトラッキング {#section-cda48fc9730142d0bb3326bac7df3271}

をサードパーティの分析システムと統合するには、 `trackEvent` viewer コールバックとプロセス `eventInfo` 必要に応じて、コールバック関数の引数です。 次のコードは、このようなハンドラー関数の例です。

```
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
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
   <td colname="col2"> <p>ビューア内でアセットが入れ替えられたとき、 <span class="codeph"> setAsset() </span> API </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p> 画像がズームされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>画像がパンされました。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWATCH </span> </p> </td> 
   <td colname="col2"> <p> スウォッチをクリックまたはタップすると画像が変更されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAGE </span> </p> </td> 
   <td colname="col2"> <p> 現在のフレームは、メインビューで変更されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ITEM </span> </p> </td> 
   <td colname="col2"> <p>情報パネルのポップアップがアクティブになります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>ユーザーが画像マップをクリックしたので、別のページに移動した。 </p> </td> 
  </tr> 
 </tbody> 
</table>
