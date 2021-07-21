---
description: ネスト/埋め込みの画像サービング要求および画像レンダリング要求で生成される中間画像データは、ネスト/埋め込み要求でcache=onを指定することでキャッシュできます。 このデータは、応答データキャッシュ内の専用の形式で保存されます。
solution: Experience Manager
title: 補助的なデータキャッシュ
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# 補助的なデータキャッシュ{#auxiliary-data-caches}

ネスト/埋め込みの画像サービング要求および画像レンダリング要求で生成される中間画像データは、ネスト/埋め込み要求でcache=onを指定することでキャッシュできます。 このデータは、応答データキャッシュ内の専用の形式で保存されます。

外部HTTPサーバーから取得した画像も応答データキャッシュに保存されます。 このようなイメージは、キャッシュエントリが生成される前に、検証ユーティリティで自動的に検証されます。

Platform Serverは、効率的なアクセスを実現するために画像カタログデータをコンパイルします。 このデータは`CS::CatalogCacheFolder`に保存されます。
