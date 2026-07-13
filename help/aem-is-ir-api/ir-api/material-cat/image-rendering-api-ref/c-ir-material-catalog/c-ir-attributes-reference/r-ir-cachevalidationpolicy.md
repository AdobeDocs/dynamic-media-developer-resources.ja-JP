---
title: CacheValidationPolicy
description: サーバーキャッシュ検証ポリシー。 サーバーサイド キャッシュ エントリを検証するタイミングを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e52577ba-d085-41f5-ad15-48e5a319e344
TQID: 'https://experienceleague.adobe.com/8WipxBM2HngJP5f8LOJmFPA5jZTyJt6Q5P9mZnzDPsY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 114
ht-degree: 2%

---

# CacheValidationPolicy{#cachevalidationpolicy}

サーバーキャッシュ検証ポリシー。 サーバーサイド キャッシュ エントリを検証するタイミングを指定します。

有効期限ベースの検証では、ソース素材と周辺光量補正が定期的にチェックされ、変更されたかどうかを確認します。 カタログベースの検証では、ソース画像は`catalog::TimeStamp`値が変更された後でのみチェックされます。

マテリアルカタログと周辺光量補正カタログの両方を使用する場合は、カタログベースの検証をお勧めします。 有効期限ベースの検証は、画像レンダリングリクエストでビネットがパスによって直接参照される場合に使用します。

## プロパティ {#section-46e13cb341eb442c86e0d8292de23ea0}

列挙： 0を指定して、有効期限ベースの検証を選択します。 1：カタログベースのキャッシュ検証を選択します。

## 初期設定 {#section-e09f3af8b6b3497d963199988dc5345d}

定義されていない場合や空の場合は、`default::CacheValidationPolicy`から継承されます。

## 関連項目 {#section-b374e4d908e24af8995b2b376ca1be8b}

[カタログ：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)

