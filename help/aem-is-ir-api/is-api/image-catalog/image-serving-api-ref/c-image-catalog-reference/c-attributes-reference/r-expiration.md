---
description: デフォルトのクライアントキャッシュの有効期間。 特定のカタログレコードに有効なカタログの有効期限の値が含まれていない場合のデフォルトの有効期限間隔を指定します。
solution: Experience Manager
title: 有効期限
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: c9dccf8d-56b3-4608-ac05-9c17babc609e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---

# 有効期限{#expiration}

デフォルトのクライアントキャッシュの有効期間。 特定のカタログレコードに有効なcatalog::Expiration値が含まれない場合のデフォルトの有効期限間隔を指定します。

## プロパティ {#section-063be3b2f13a48a3a5ab8080718e9812}

0以上の実数。 応答データが生成されてから有効期限が切れるまでの時間数。 0に設定すると、常に返信イメージの有効期限が即座に切れ、クライアントのキャッシュが効果的に無効になります。 -1に設定すると、`never expire`としてマークされます。

## 初期設定 {#section-f55308b195c04083996f6717c8537634}

`default::Expiration`から継承されます（定義されていない場合または空の場合）。

TTL(Time-To-Live)は、キャッシュが期限切れになるまでの期間です。 デフォルトのTTLは10時間です。

## 関連項目 {#section-b2411d99ddb14115ad475d506efd8967}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) 、 [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)、 [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
