---
description: キャッシュクラスタリングには、これらのサーバー設定を使用します。
solution: Experience Manager
title: キャッシュクラスタリング
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: bd0267e7-ebf5-4995-b55e-89cb1a58de6d
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# キャッシュクラスタリング{#cache-clustering}

キャッシュクラスタリングには、これらのサーバー設定を使用します。

## PS::cacheCluster.hosts — ホスト {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

IPアドレスをセミコロンで区切ったリスト。 このホストがキャッシュデータを取得する必要があるすべてのピアサーバのIPアドレスを含めます。 ローカルホストのIPアドレスは、便宜上、含めてもよい。これにより、クラスター内のすべてのサーバーに対して同じ構成設定が可能になります。

## PS::cacheCluster.updateLocalCache — ローカルキャッシュを更新 {#section-154c2c0af4544200a3499232bb130dde}

ピアサーバーが提供するキャッシュエントリをローカル応答キャッシュにコピーする必要がある場合は、「はい」に設定します。

## PS::cacheCluster.queryTimeout — クエリタイムアウト {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

ピアサーバからキャッシュエントリを要求する際、サーバは、1台のサーバがこの特定のデータ項目を持つと応答するか、すべてのピアサーバがデータ項目を持たないと応答するか、この設定で指定した時間（ミリ秒）が切れるまで待ちます。

## PS::cacheCluster.fetchTimeout — フェッチタイムアウト {#section-41c42a29a26f43dc9cff50ad9fae1f14}

ピアサーバから実際のキャッシュデータが配信されるのをサーバが待機する最大ミリ秒数を指定します。 タイムアウトの期限が切れる前に完全なデータが配信されなかった場合、サーバはピアが使用できなくなったと見なします。 その後、キャッシュエントリがローカルに生成されます。
