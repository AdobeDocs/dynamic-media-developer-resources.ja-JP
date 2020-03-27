---
description: eCatalog検索ビューアでは、Adobe Analyticsの追跡機能がサポートされていて、この機能をすぐに使用できます。
seo-description: eCatalog検索ビューアでは、Adobe Analyticsの追跡機能がサポートされていて、この機能をすぐに使用できます。
seo-title: Adobe Analyticsの追跡のサポート
solution: Experience Manager
title: Adobe Analyticsの追跡のサポート
topic: Dynamic media
uuid: 2e1e2bc6-5372-4ba2-b6d7-8b760b1b0a8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Adobe Analyticsの追跡のサポート{#support-for-adobe-analytics-tracking}

eCatalog検索ビューアでは、Adobe Analyticsの追跡機能がサポートされていて、この機能をすぐに使用できます。

## 追跡機能をすぐに使用できる機能 {#section-ba994f079d0343c8ae48adffaa3195a3}

eCatalog検索ビューアでは、追 [!DNL Adobe Analytics] 跡機能がサポートされていて、この機能をすぐに使用できます。 追跡を有効にするには、適切な会社プリセット名をパラメーターとして渡 `config2` します。

また、ビューアは、設定済みのImage Serverに対して、ビューアのタイプとバージョン情報と共に単一の追跡HTTP要求を送信します。

## カスタム追跡 {#section-cda48fc9730142d0bb3326bac7df3271}

サードパーティの分析システムと統合するには、ビューアのコールバックをリッスンし、必要に応じ `trackEvent` てコールバック関数の `eventInfo` 引数を処理する必要があります。 次のコードは、このようなハンドラー関数の例です。

```
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
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
   <td colname="col2"> <p> 画像がズームされた。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> PAGE </span> </p> </td> 
   <td colname="col2"> <p> 現在のフレームがメインビューで変更された場合。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ITEM </span> </p> </td> 
   <td colname="col2"> <p>情報パネルのポップアップがアクティブになります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>ユーザが画像マップをクリックしたために別のページに移動した場合。 </p> </td> 
  </tr> 
 </tbody> 
</table>

