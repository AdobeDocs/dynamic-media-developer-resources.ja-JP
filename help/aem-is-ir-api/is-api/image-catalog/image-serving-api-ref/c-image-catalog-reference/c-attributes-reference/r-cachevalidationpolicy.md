---
description: サーバーキャッシュ検証ポリシー。 サーバー側のキャッシュエントリを検証するタイミングを指定します。
solution: Experience Manager
title: CacheValidationPolicy
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: d54a8ab9-d6b3-4eae-95c6-c4ab6f00ebde
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---

# CacheValidationPolicy{#cachevalidationpolicy}

サーバーキャッシュ検証ポリシー。 サーバー側のキャッシュエントリを検証するタイミングを指定します。

有効期限ベースの検証では、ソース画像が変更されたかどうかが定期的にチェックされます。 カタログベースの検証では、ソース画像は`catalog::TimeStamp`の値が変更された後にのみ確認されます。

画像カタログを使用する場合は、カタログベースの検証をお勧めします。 画像カタログを使用せずに画像を直接参照する場合は、有効期限ベースの検証を使用する必要があります。

## プロパティ {#section-650cbddd81a24c3b8b70479248a45dc9}

列挙 「0」の場合は有効期限ベースの検証を選択し、「1」の場合はカタログベースのキャッシュ検証を選択します。

## 初期設定 {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

`default::CacheValidationPolicy`から継承されます（定義されていない場合または空の場合）。

## 関連項目 {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
