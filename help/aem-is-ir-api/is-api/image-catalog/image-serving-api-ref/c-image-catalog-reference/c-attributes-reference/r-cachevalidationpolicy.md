---
title: CacheValidationPolicy
description: サーバーキャッシュの検証ポリシーです。 サーバー側のキャッシュエントリを検証するタイミングを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d54a8ab9-d6b3-4eae-95c6-c4ab6f00ebde
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 4%

---

# CacheValidationPolicy{#cachevalidationpolicy}

サーバーキャッシュの検証ポリシーです。 サーバー側のキャッシュエントリを検証するタイミングを指定します。

有効期限ベースの検証では、ソース画像が変更されたかどうかが定期的に確認されます。 カタログベースの検証では、ソース画像は `catalog::TimeStamp` の値が変更されました。

画像カタログを使用する場合は、カタログベースの検証をお勧めします。 画像カタログを使用せずに画像が直接参照される場合は、有効期限ベースの検証を使用する必要があります。

## プロパティ {#section-650cbddd81a24c3b8b70479248a45dc9}

列挙。 0 ：有効期限ベースの検証を選択し、1 ：カタログベースのキャッシュ検証を選択します。

## 初期設定 {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

継承元 `default::CacheValidationPolicy` が定義されていない場合、または空の場合は。

## 関連項目 {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
