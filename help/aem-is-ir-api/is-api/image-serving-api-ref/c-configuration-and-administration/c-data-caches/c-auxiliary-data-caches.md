---
description: ネスト/埋め込みの画像サービング要求と画像レンダリング要求で生成される中間画像データは、ネスト/埋め込みの要求でcache=onを指定することでキャッシュできます。 このデータは、応答データキャッシュ内の独自の形式で保存されます。
seo-description: ネスト/埋め込みの画像サービング要求と画像レンダリング要求で生成される中間画像データは、ネスト/埋め込みの要求でcache=onを指定することでキャッシュできます。 このデータは、応答データキャッシュ内の独自の形式で保存されます。
seo-title: 補助的なデータキャッシュ
solution: Experience Manager
title: 補助的なデータキャッシュ
topic: Scene7 Image Serving - Image Rendering API
uuid: 10ce998e-e300-4d24-9d92-a8693dade327
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# 補助的なデータキャッシュ{#auxiliary-data-caches}

ネスト/埋め込みの画像サービング要求と画像レンダリング要求で生成される中間画像データは、ネスト/埋め込みの要求でcache=onを指定することでキャッシュできます。 このデータは、応答データキャッシュ内の独自の形式で保存されます。

外部のHTTPサーバから取得した画像も応答データキャッシュに格納されます。 このようなイメージは、キャッシュエントリが生成される前に、validateユーティリティで自動的に検証されます。

プラットフォームサーバは、効率的なアクセスを実現するために画像カタログデータをコンパイルします。 このデータは`CS::CatalogCacheFolder`に保存されます。
