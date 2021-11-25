---
title: Adobe Analytics追跡のサポート
description: Adobe Analytics追跡のサポート
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User,Data Engineer,Data Architect
exl-id: fb58a388-e4da-475d-b726-d5a32e99cce0
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 1%

---

# Adobe Analytics追跡のサポート{#support-for-adobe-analytics-tracking}

デフォルトでは、ビューアは、設定済みの Image Server に対し、ビューアのタイプとバージョン情報を含む単一のトラッキング HTTP 要求を送信します。

## カスタムトラッキング {#section-cda48fc9730142d0bb3326bac7df3271}

をサードパーティの分析システムと統合するには、をリッスンする必要があります。 `trackEvent` ビューアのコールバックとプロセス `eventInfo` 必要に応じて、コールバック関数の引数です。 次のコードは、このようなハンドラー関数の例です。

```
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

ビューアは、次の SDK ユーザーイベントを追跡します。

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK ユーザーイベント </p> </th> 
   <th colname="col2" class="entry"> <p>送信済み… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>ビューアが最初に読み込まれたとき。 </p> </td> 
  </tr> 
 </tbody> 
</table>
