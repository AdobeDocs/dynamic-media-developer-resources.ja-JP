---
title: Adobe Analytics トラッキングのサポート
description: スピンビューアは、標準搭載のAdobe Analytics トラッキングをサポートしています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 30762700-6d69-4299-9492-57893232abe1
TQID: 'https://experienceleague.adobe.com/a9Ab9GwdXqTOrBLuKj49d5Jl01V2-iGH5xb1khFGH7g'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 163
ht-degree: 0%

---

# Adobe Analytics トラッキングのサポート{#support-for-adobe-analytics-tracking}

スピンビューアは、標準搭載のAdobe Analytics トラッキングをサポートしています。

## すぐに利用できるトラッキング機能 {#section-d06145cfa2b9491bb485b599368d466e}

スピンビューアは、Adobe Analyticsのトラッキングをすぐにサポートします。

トラッキングを有効にするには、適切な会社プリセット名を`config2` パラメーターとして渡します。

ビューアは、ビューアのタイプとバージョン情報を使用して、設定されたImage Serverに1つのトラッキング HTTP リクエストを送信します。

## カスタムトラッキング {#section-47512156a1d64b338b50cfa39c84f4aa}

サードパーティの分析システムと統合するには、`trackEvent` ビューアのコールバックをリッスンし、必要に応じてコールバック関数の`eventInfo`引数を処理する必要があります。 以下のコードは、そのようなハンドラー関数の例です。

```javascript {.line-numbers}
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
   <td colname="col1"> <p> <span class="codeph"> ズーム </span> </p> </td> 
   <td colname="col2"> <p> 画像はズームされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">計画</span> </p> </td> 
   <td colname="col2"> <p>画像が計画されています。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> スピン </span> </p> </td> 
   <td colname="col2"> <p> スピンが行われます。 </p> </td> 
  </tr> 
 </tbody> 
</table>
