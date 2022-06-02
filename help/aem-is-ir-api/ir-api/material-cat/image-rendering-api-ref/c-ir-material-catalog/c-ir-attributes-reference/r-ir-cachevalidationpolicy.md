---
title: CacheValidationPolicy
description: サーバーキャッシュの検証ポリシーです。 サーバー側のキャッシュエントリを検証するタイミングを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e52577ba-d085-41f5-ad15-48e5a319e344
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---

# CacheValidationPolicy{#cachevalidationpolicy}

サーバーキャッシュの検証ポリシーです。 サーバー側のキャッシュエントリを検証するタイミングを指定します。

有効期限ベースの検証では、ソース素材とビネットが定期的にチェックされ、変更されたかどうかが確認されます。 カタログベースの検証では、ソース画像は `catalog::TimeStamp` の値が変更されました。

マテリアルカタログとビネットカタログの両方を使用する場合は、カタログベースの検証をお勧めします。 ビネットが画像レンダリング要求でパスで直接参照される場合は、有効期限に基づく検証を使用する必要があります。

## プロパティ {#section-46e13cb341eb442c86e0d8292de23ea0}

列挙。 0 を指定すると、有効期限に基づく検証が選択されます。 1：カタログベースのキャッシュ検証を選択します。

## 初期設定 {#section-e09f3af8b6b3497d963199988dc5345d}

継承元 `default::CacheValidationPolicy` が定義されていない場合、または空の場合は。

## 関連項目 {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
