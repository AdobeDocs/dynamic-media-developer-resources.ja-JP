---
description: サーバーキャッシュの検証ポリシー。 サーバー側のキャッシュエントリを検証するタイミングを指定します。
solution: Experience Manager
title: CacheValidationPolicy
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---


# CacheValidationPolicy{#cachevalidationpolicy}

サーバーキャッシュの検証ポリシー。 サーバー側のキャッシュエントリを検証するタイミングを指定します。

有効期限ベースの検証では、ソース素材とビネットが定期的にチェックされ、ビネットが変更されたかどうかを確認します。 カタログベースの検証では、ソース画像は`catalog::TimeStamp`値が変更された後にのみチェックされます。

マテリアルカタログとビネットカタログの両方を使用する場合は、カタログベースの検証をお勧めします。 ビネットが画像レンダリング要求で直接パスで参照される場合、有効期限に基づく検証を使用する必要があります。

## プロパティ {#section-46e13cb341eb442c86e0d8292de23ea0}

列挙。 0を指定すると、有効期限ベースの検証が選択されます。 1を指定します。

## 初期設定 {#section-e09f3af8b6b3497d963199988dc5345d}

定義されていない場合や空の場合は`default::CacheValidationPolicy`から継承されます。

## 関連項目 {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
