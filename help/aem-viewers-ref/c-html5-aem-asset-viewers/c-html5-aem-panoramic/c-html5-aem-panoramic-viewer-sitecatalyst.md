---
title: Adobe Analytics トラッキングのサポート
description: Adobe Analytics トラッキングのサポート
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: fb58a388-e4da-475d-b726-d5a32e99cce0
autotag-review: '2026-05-13T22:16:55.117Z'
TQID: 'https://experienceleague.adobe.com/vNBqF1nJS9wJrXRDlGelxVA5rwUpeoSkaSTV3qu-hhY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 92
ht-degree: 0%

---

# Adobe Analytics トラッキングのサポート{#support-for-adobe-analytics-tracking}

デフォルトでは、ビューアは、ビューアのタイプとバージョン情報を含む設定されたImage Serverに1つのトラッキング HTTP リクエストを送信します。

## カスタムトラッキング {#section-cda48fc9730142d0bb3326bac7df3271}

サードパーティの分析システムと統合するには、`trackEvent` ビューアのコールバックをリッスンし、必要に応じてコールバック関数の`eventInfo`引数を処理する必要があります。 以下のコードは、そのようなハンドラー関数の例です。

```javascript {.line-numbers}
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
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
   <th colname="col2" class="entry"> <p>送信済… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">を読み込み</span> </p> </td> 
   <td colname="col2"> <p>ビューアが最初に読み込まれるとき。 </p> </td> 
  </tr> 
 </tbody> 
</table>
