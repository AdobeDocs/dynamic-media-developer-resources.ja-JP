---
title: setAsset
description: Video360 ViewerのJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 1fcd7dbe-d122-4501-92f4-3ce93a94a933
TQID: 'https://experienceleague.adobe.com/lTQFHvRluUdTkFdxirXbJ50cvmJLmV10439fPd7VxnY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 53
ht-degree: 3%

---

# setAsset{#setasset}

Video360 ViewerのJavaScript API リファレンス。

`setAsset(asset)`

新しいアセットを設定します。 このパラメーターは、`init()`の前または後に、いつでも呼び出すことができます。 `init()`の後に呼び出された場合、ビューアは実行時にアセットを入れ替えます。

[init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)も参照してください。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> アセット </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph">文字列</span>}個の新しいアセット ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Viewers/space_station_360-AVS")
```
