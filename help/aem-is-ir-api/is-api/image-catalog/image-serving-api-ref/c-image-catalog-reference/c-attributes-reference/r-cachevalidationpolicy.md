---
title: CacheValidationPolicy
description: サーバーキャッシュ検証ポリシー。 サーバーサイド キャッシュ エントリを検証するタイミングを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d54a8ab9-d6b3-4eae-95c6-c4ab6f00ebde
TQID: 'https://experienceleague.adobe.com/s7dYUadAD1i1ROqCafEZOa5Tztl3ss2HAXnEsPiRGr8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 2%

---

# CacheValidationPolicy{#cachevalidationpolicy}

サーバーキャッシュ検証ポリシー。 サーバーサイド キャッシュ エントリを検証するタイミングを指定します。

有効期限ベースの検証では、ソースイメージが変更されたかどうかを定期的にチェックします。 カタログベースの検証では、ソース画像は`catalog::TimeStamp`値が変更された後でのみチェックされます。

画像カタログを使用する場合は、カタログベースの検証をお勧めします。 有効期限ベースの検証は、画像カタログを使用せずに画像を直接参照する場合に使用する必要があります。

## プロパティ {#section-650cbddd81a24c3b8b70479248a45dc9}

列挙： 有効期限ベースの検証を選択するには0を、カタログベースのキャッシュ検証を選択するには1を指定します。

## 初期設定 {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

定義されていない場合や空の場合は、`default::CacheValidationPolicy`から継承されます。

## 関連項目 {#section-a0c922fa519641f2bce05e75e4eb51d0}

[カタログ：:TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
