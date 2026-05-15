---
description: ネスト/埋め込み画像サービング要求と画像レンダリング要求によって生成された中間画像データは、ネスト/埋め込み要求でcache=onを指定することでキャッシュできます。 このデータは、応答データキャッシュに独自の形式で保存されます。
solution: Experience Manager
title: 補助データキャッシュ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
TQID: 'https://experienceleague.adobe.com/oRZFSXKaBE9q7liBPRVCheL-NPTriPJkWZFqgMBcoaQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 122
ht-degree: 0%

---

# 補助データキャッシュ{#auxiliary-data-caches}

ネスト/埋め込み画像サービング要求と画像レンダリング要求によって生成された中間画像データは、ネスト/埋め込み要求でcache=onを指定することでキャッシュできます。 このデータは、応答データキャッシュに独自の形式で保存されます。

外部のHTTP サーバーから取得した画像も、応答データキャッシュに格納されます。 そのような画像は、キャッシュエントリが生成される前に、validate ユーティリティで自動的に検証されます。

[!DNL Platform Server]は、効率的なアクセスのために画像カタログデータをコンパイルします。 このデータは`CS::CatalogCacheFolder`に保存されています。
