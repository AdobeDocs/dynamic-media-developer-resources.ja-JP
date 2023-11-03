---
description: キャッシュクラスタリングには、次のサーバー設定を使用します。
solution: Experience Manager
title: キャッシュクラスタリング
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: bd0267e7-ebf5-4995-b55e-89cb1a58de6d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# キャッシュクラスタリング{#cache-clustering}

キャッシュクラスタリングには、次のサーバー設定を使用します。

## PS::cacheCluster.hosts — ホスト {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

IP アドレスのリスト（セミコロンで区切る）。 このホストがキャッシュデータを取得する必要があるすべてのピアサーバの IP アドレスを含めます。 ローカルホストの IP アドレスは、便宜上、含めることができます。これにより、クラスタ内のすべてのサーバーに対して同じ設定を行うことができます。

## PS::cacheCluster.updateLocalCache — ローカルキャッシュを更新 {#section-154c2c0af4544200a3499232bb130dde}

ピアサーバが提供するキャッシュエントリをローカル応答キャッシュにコピーする必要がある場合は、「はい」に設定します。

## PS::cacheCluster.queryTimeout — クエリタイムアウト {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

ピアサーバからキャッシュエントリを要求する際、サーバは、1 台のサーバがこの特定のデータ項目を持つと応答するか、すべてのピアサーバがデータ項目を持たないと応答するまで、またはこの設定で指定された時間（ミリ秒）が経過するまで待ちます。

## PS::cacheCluster.fetchTimeout — 取得タイムアウト {#section-41c42a29a26f43dc9cff50ad9fae1f14}

サーバがピアサーバから実際のキャッシュデータが配信されるのを待機する最大ミリ秒数を指定します。 タイムアウトが切れる前に完全なデータが配信されなかった場合、サーバはピアが使用できなくなったと見なします。 その後、キャッシュエントリがローカルに生成されます。
