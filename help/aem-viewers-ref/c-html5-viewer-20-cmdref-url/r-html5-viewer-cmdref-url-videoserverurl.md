---
title: videoServerUrl
description: すべてのビューアに共通のパラメーター。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db0ce8c4-3754-4fef-9430-44ee8e5c5e80
TQID: 'https://experienceleague.adobe.com/rHcYe13DDclS1Y7rguOHBuAGP-IH9oxzqpp7uorHc2Y'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 63
ht-degree: 4%

---

# videoServerUrl{#videoserverurl}

すべてのビューアに共通のパラメーター。

>[!NOTE]
>
>このコマンドは、ビデオ画像ビューアには適用されません。

` videoServerUrl= *`videoRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> ビデオサーバーのルートパス。 ドメインが指定されていない場合は、ページが提供されるドメインが代わりに適用されます。 標準のURI パス解決が適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-10ee45d637134e0fbcd943c62578cb78}

オプション。 サービスとして標準的なソフトウェアを使用する場合は必要ありません。

## 初期設定 {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## 例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
