---
description: サーバーキャッシュの検証ポリシー。 サーバー側のキャッシュエントリを検証するタイミングを指定します。
solution: Experience Manager
title: CacheValidationPolicy
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---


# CacheValidationPolicy{#cachevalidationpolicy}

サーバーキャッシュの検証ポリシー。 サーバー側のキャッシュエントリを検証するタイミングを指定します。

有効期限ベースの検証では、ソース画像が変更されたかどうかが定期的にチェックされます。 カタログベースの検証では、ソース画像は`catalog::TimeStamp`値が変更された後にのみチェックされます。

画像カタログを使用する場合は、カタログベースの検証をお勧めします。 有効期限ベースの検証は、画像が画像カタログを使用せずに直接参照される場合に使用します。

## プロパティ {#section-650cbddd81a24c3b8b70479248a45dc9}

列挙。 0の場合は有効期限ベースの検証を、1の場合はカタログベースのキャッシュ検証を選択します。

## 初期設定 {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

定義されていない場合や空の場合は`default::CacheValidationPolicy`から継承されます。

## 関連項目 {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
