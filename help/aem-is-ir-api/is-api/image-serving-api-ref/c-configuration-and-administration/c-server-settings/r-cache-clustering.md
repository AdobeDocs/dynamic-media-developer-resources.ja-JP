---
description: キャッシュクラスタリングには、次のサーバー設定を使用します。
solution: Experience Manager
title: キャッシュクラスタリング
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# キャッシュクラスタリング{#cache-clustering}

キャッシュクラスタリングには、次のサーバー設定を使用します。

## PS::cacheCluster.hosts — ホスト{#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

IPアドレスをセミコロンで区切ってリストします。 このホストがキャッシュデータを取得するすべてのピアサーバのIPアドレスを含めます。 便宜上、ローカルホストのIPアドレスを含めてもよい。これにより、クラスター内のすべてのサーバーに対して同じ設定を行うことができます。

## PS::cacheCluster.updateLocalCache — ローカルキャッシュを更新する{#section-154c2c0af4544200a3499232bb130dde}

ピアサーバーが提供するキャッシュエントリをローカル応答キャッシュにコピーする場合は、「Yes」に設定します。

## PS::cacheCluster.queryTimeout -クエリタイムアウト{#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

ピアサーバーからキャッシュエントリを要求すると、サーバーは、特定のデータ項目を持つという応答が1つのサーバーから返されるか、またはすべてのピアサーバーがデータ項目を持たないと応答するか、この設定で指定された時間（ミリ秒）が経過するまで待ちます。

## PS::cacheCluster.fetchTimeout — フェッチタイムアウト{#section-41c42a29a26f43dc9cff50ad9fae1f14}

ピアサーバから実際のキャッシュデータが配信されるのをサーバが待機する最大ミリ秒数を指定します。 タイムアウトが切れる前に完全なデータが配信されなかった場合、サーバはピアが使用不可になったと見なします。 その後、キャッシュエントリがローカルに生成されます。
