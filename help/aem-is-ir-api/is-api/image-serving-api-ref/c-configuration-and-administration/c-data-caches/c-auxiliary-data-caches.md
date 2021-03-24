---
description: ネスト/埋め込みの画像サービング要求と画像レンダリング要求で生成される中間画像データは、ネスト/埋め込みの要求でcache=onを指定することでキャッシュできます。 このデータは、応答データキャッシュ内の独自の形式で保存されます。
solution: Experience Manager
title: 補助的なデータキャッシュ
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# 補助的なデータキャッシュ{#auxiliary-data-caches}

ネスト/埋め込みの画像サービング要求と画像レンダリング要求で生成される中間画像データは、ネスト/埋め込みの要求でcache=onを指定することでキャッシュできます。 このデータは、応答データキャッシュ内の独自の形式で保存されます。

外部のHTTPサーバから取得した画像も応答データキャッシュに格納されます。 このようなイメージは、キャッシュエントリが生成される前に、validateユーティリティで自動的に検証されます。

プラットフォームサーバは、効率的なアクセスを実現するために画像カタログデータをコンパイルします。 このデータは`CS::CatalogCacheFolder`に保存されます。
