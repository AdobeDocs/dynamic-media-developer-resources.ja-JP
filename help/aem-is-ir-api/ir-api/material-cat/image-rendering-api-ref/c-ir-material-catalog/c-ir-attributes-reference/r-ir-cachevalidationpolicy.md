---
title: CacheValidationPolicy
description: サーバーキャッシュ検証ポリシー。 サーバーサイド キャッシュ エントリを検証するタイミングを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e52577ba-d085-41f5-ad15-48e5a319e344
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 2%

---

# CacheValidationPolicy{#cachevalidationpolicy}

サーバーキャッシュ検証ポリシー。 サーバーサイド キャッシュ エントリを検証するタイミングを指定します。

有効期限ベースの検証では、ソースのマテリアルとビネットが変更されたかどうかを定期的に確認します。 カタログベースの検証では、`catalog::TimeStamp` 値が変更された後にのみ、ソース画像がチェックされます。

材料カタログとビネットカタログの両方を使用する場合は、カタログベースの検証をお勧めします。 画像レンダリングリクエストでビネットがパスによって直接参照される場合は、有効期限ベースの検証を使用する必要があります。

## プロパティ {#section-46e13cb341eb442c86e0d8292de23ea0}

列挙値。 0 を指定すると、有効期限ベースの検証が選択されます。 1：カタログベースのキャッシュ検証を選択します。

## 初期設定 {#section-e09f3af8b6b3497d963199988dc5345d}

定義されていない場合または空の場合は `default::CacheValidationPolicy` から継承します。

## 関連項目 {#section-b374e4d908e24af8995b2b376ca1be8b}

[カタログ：：タイムスタンプ](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
