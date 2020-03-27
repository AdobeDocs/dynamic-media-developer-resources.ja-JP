---
description: サーバーキャッシュの検証ポリシー。 サーバー側のキャッシュエントリを検証するタイミングを指定します。
seo-description: サーバーキャッシュの検証ポリシー。 サーバー側のキャッシュエントリを検証するタイミングを指定します。
seo-title: CacheValidationPolicy
solution: Experience Manager
title: CacheValidationPolicy
topic: Scene7 Image Serving - Image Rendering API
uuid: 299dd5fe-9a0c-43df-a4c8-6b9e9c24003b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CacheValidationPolicy{#cachevalidationpolicy}

サーバーキャッシュの検証ポリシー。 サーバー側のキャッシュエントリを検証するタイミングを指定します。

有効期限ベースの検証では、ソースマテリアルとビネットが定期的にチェックされ、変更されたかどうかが確認されます。 カタログベースの検証では、値が変更された後にのみソース画像がチェ `catalog::TimeStamp` ックされます。

マテリアルカタログとビネットカタログの両方を使用する場合は、カタログベースの検証をお勧めします。 ビネットが画像レンダリング要求内でパスで直接参照される場合は、有効期限に基づく検証を使用する必要があります。

## プロパティ {#section-46e13cb341eb442c86e0d8292de23ea0}

列挙。 0を指定すると、有効期限に基づく検証が選択されます。 1を指定します。

## 初期設定 {#section-e09f3af8b6b3497d963199988dc5345d}

定義されていな `default::CacheValidationPolicy` い場合や空の場合に継承されます。

## 関連項目 {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
