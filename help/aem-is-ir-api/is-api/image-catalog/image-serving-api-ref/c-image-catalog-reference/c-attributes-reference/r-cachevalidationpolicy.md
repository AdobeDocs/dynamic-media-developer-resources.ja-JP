---
description: サーバーキャッシュの検証ポリシー。 サーバー側のキャッシュエントリを検証するタイミングを指定します。
seo-description: サーバーキャッシュの検証ポリシー。 サーバー側のキャッシュエントリを検証するタイミングを指定します。
seo-title: CacheValidationPolicy
solution: Experience Manager
title: CacheValidationPolicy
topic: Scene7 Image Serving - Image Rendering API
uuid: 371dadbf-d58e-4214-8050-7e8907b436e3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CacheValidationPolicy{#cachevalidationpolicy}

サーバーキャッシュの検証ポリシー。 サーバー側のキャッシュエントリを検証するタイミングを指定します。

有効期限ベースの検証では、ソース画像が変更されたかどうかが定期的に確認されます。 カタログベースの検証では、値が変更された後にのみソース画像がチェ `catalog::TimeStamp` ックされます。

画像カタログを使用する場合は、カタログベースの検証をお勧めします。 有効期限ベースの検証は、画像が画像カタログを使用せずに直接参照される場合に使用します。

## プロパティ {#section-650cbddd81a24c3b8b70479248a45dc9}

列挙。 0を指定すると有効期限ベースの検証が選択され、1を指定するとカタログベースのキャッシュ検証が選択されます。

## 初期設定 {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

定義されていな `default::CacheValidationPolicy` い場合や空の場合に継承されます。

## 関連項目 {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
