---
description: これらのサーバー設定をキャッシュ クラスタリングに使用します。
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

これらのサーバー設定をキャッシュ クラスタリングに使用します。

## PS::cacheCluster.hosts - ホスト {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

セミコロンで区切られた IP アドレスのリスト。 このホストがキャッシュデータを取得する必要があるすべてのピアサーバーの IP アドレスを含めます。 便宜上、ローカルホストの IP アドレスを含めることができます。これにより、クラスター内のすべてのサーバーで同じ設定が可能になります。

## PS::cacheCluster.updateLocalCache - ローカルキャッシュを更新する {#section-154c2c0af4544200a3499232bb130dde}

ピアサーバーによって提供されたキャッシュエントリをローカル応答キャッシュにコピーする必要がある場合は、「はい」に設定します。

## PS::cacheCluster.queryTimeout - クエリタイムアウト {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

ピア サーバーからキャッシュ エントリを要求する場合、サーバーは 1 つのサーバーがこの特定のデータ アイテムを持っていることを応答するまで、またはすべてのピア サーバーがデータ アイテムを持っていないことを応答するまで、またはこの設定で指定された時間（ミリ秒）が経過するまで待機します。

## PS::cacheCluster.fetchTimeout - Fetch Timeout {#section-41c42a29a26f43dc9cff50ad9fae1f14}

ピア サーバーから実際のキャッシュ データが配信されるまで、サーバーが待機する最大時間（ミリ秒）を指定します。 タイムアウトの期限が切れる前に完全なデータが配信されなかった場合、サーバはピアが使用不可になったと見なします。 次に、キャッシュエントリがローカルに生成されます。
