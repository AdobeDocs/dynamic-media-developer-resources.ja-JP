---
description: キャッシュクラスタリングには、これらのサーバー設定を使用します。
solution: Experience Manager
title: キャッシュクラスタリング
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: bd0267e7-ebf5-4995-b55e-89cb1a58de6d
TQID: 'https://experienceleague.adobe.com/4SJmK1ILgnCBqYjjQcEnz0SVRzQfsY9mD05Xpd1ssnw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 200
ht-degree: 0%

---

# キャッシュクラスタリング{#cache-clustering}

キャッシュクラスタリングには、これらのサーバー設定を使用します。

## PS::cacheCluster.hosts - Hosts {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

セミコロンで区切られたIP アドレスのリスト。 このホストがキャッシュデータを取得する必要があるすべてのピアサーバーのIP アドレスを含めます。 ローカルホストのIP アドレスは、便宜のために含めることができます。これにより、クラスター内のすべてのサーバーで同じ設定設定が可能になります。

## PS::cacheCluster.updateLocalCache - ローカルキャッシュの更新 {#section-154c2c0af4544200a3499232bb130dde}

ピアサーバーが提供するキャッシュエントリをローカル応答キャッシュにコピーする必要がある場合は、「はい」に設定します。

## PS::cacheCluster.queryTimeout - クエリタイムアウト {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

ピアサーバーからキャッシュエントリを要求する場合、サーバーは、1つのサーバーがこの特定のデータ項目を持っていると応答するか、すべてのピアサーバーがデータ項目を持っていないと応答するか、この設定で指定された時間（ミリ秒）が経過するまで待機します。

## PS::cacheCluster.fetchTimeout - Fetch Timeout {#section-41c42a29a26f43dc9cff50ad9fae1f14}

ピア サーバーから実際のキャッシュ データが配信されるのをサーバーが待機する最大ミリ秒数を指定します。 タイムアウトが終了する前に完全なデータが配信されていない場合、サーバーはピアが利用できないと仮定します。 その後、キャッシュエントリはローカルで生成されます。
