---
description: デフォルトのクライアントキャッシュの有効期限。 特定のカタログレコードに有効なカタログ有効期限の値が含まれていない場合に使用する、デフォルトの有効期限間隔を指定します。
solution: Experience Manager
title: 有効期限
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9dccf8d-56b3-4608-ac05-9c17babc609e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---

# 有効期限{#expiration}

デフォルトのクライアントキャッシュの有効期限。 特定のカタログレコードに有効なカタログ：:Expiration 値が含まれていない場合に使用する、デフォルトの有効期限間隔を指定します。

## プロパティ {#section-063be3b2f13a48a3a5ab8080718e9812}

0 以上の実数。 返信データが生成されてから有効期限が切れるまでの時間数。 常に返信画像をすぐに期限切れにする場合は 0 に設定します。これにより、クライアントのキャッシュが効果的に無効になります。 -1 に設定すると、`never expire` としてマークされます。

## 初期設定 {#section-f55308b195c04083996f6717c8537634}

定義されていない場合または空の場合は `default::Expiration` から継承します。

TTL （Time-To-Live）は、キャッシュの有効期限が切れるまでの期間です。 デフォルト TTL は 10 時間です。

## 関連項目 {#section-b2411d99ddb14115ad475d506efd8967}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a)、[attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)、[attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
