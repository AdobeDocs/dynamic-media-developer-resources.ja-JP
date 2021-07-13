---
description: 基本ズームビューアでは、Adobe Analyticsの追跡機能がサポートされていて、この機能をすぐに使用できます。
solution: Experience Manager
title: Adobe Analytics追跡のサポート
feature: Dynamic Media Classic，ビューア，SDK/API，ズーム
role: Developer,User,Data Engineer,Data Architect
exl-id: 5b9d871d-9f37-4908-900e-3f0ecc98bc0c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 2%

---

# Adobe Analytics追跡のサポート{#support-for-adobe-analytics-tracking}

基本ズームビューアでは、Adobe Analyticsの追跡機能がサポートされていて、この機能をすぐに使用できます。

## 標準のトラッキング {#section-ba994f079d0343c8ae48adffaa3195a3}

基本ズームビューアでは、 [!DNL Adobe Analytics]トラッキングがサポートされていて、この機能をすぐに使用できます。 追跡を有効にするには、適切な会社プリセット名を`config2`パラメーターとして渡します。

また、ビューアは、設定済みのImage Serverに対して、ビューアのタイプとバージョン情報を含む単一の追跡HTTP要求も送信します。

## カスタムトラッキング {#section-cda48fc9730142d0bb3326bac7df3271}

サードパーティの分析システムと統合するには、 `trackEvent`ビューアコールバックをリッスンし、必要に応じてコールバック関数の`eventInfo`引数を処理する必要があります。 次のコードは、このようなハンドラー関数の例です。

```
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
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
   <th colname="col2" class="entry"> <p>送信タイミング… </p> </th> 
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
   <td colname="col2"> <p> 画像がズームされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>画像がパンされます。 </p> </td> 
  </tr> 
 </tbody> 
</table>
