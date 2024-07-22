---
title: CacheValidationPolicy
description: サーバーキャッシュ検証ポリシー。 サーバーサイド キャッシュ エントリを検証するタイミングを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d54a8ab9-d6b3-4eae-95c6-c4ab6f00ebde
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 3%

---

# CacheValidationPolicy{#cachevalidationpolicy}

サーバーキャッシュ検証ポリシー。 サーバーサイド キャッシュ エントリを検証するタイミングを指定します。

有効期限ベースの検証では、ソース画像が変更されたかどうかを定期的に確認します。 カタログベースの検証では、`catalog::TimeStamp` 値が変更された後にのみ、ソース画像がチェックされます。

画像カタログを使用する場合は、カタログベースの検証をお勧めします。 画像が画像カタログを使用せずに直接参照される場合は、有効期限ベースの検証を使用する必要があります。

## プロパティ {#section-650cbddd81a24c3b8b70479248a45dc9}

列挙値。 0 は有効期限ベースの検証を選択し、1 はカタログベースのキャッシュ検証を選択します。

## 初期設定 {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

定義されていない場合または空の場合は `default::CacheValidationPolicy` から継承します。

## 関連項目 {#section-a0c922fa519641f2bce05e75e4eb51d0}

[カタログ：：タイムスタンプ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
