---
description: デフォルトのクライアントキャッシュの有効時間。 特定のカタログレコードに有効なカタログの有効期限の値が含まれていない場合に使用する初期設定の有効期限の間隔を指定します。
seo-description: デフォルトのクライアントキャッシュの有効時間。 特定のカタログレコードに有効なカタログの有効期限の値が含まれていない場合に使用する初期設定の有効期限の間隔を指定します。
seo-title: 有効期限
solution: Experience Manager
title: 有効期限
topic: Scene7 Image Serving - Image Rendering API
uuid: 26b2abee-8bd1-4011-90ff-f5143826ac0d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 有効期限{#expiration}

デフォルトのクライアントキャッシュの有効時間。 特定のカタログレコードに有効なcatalog::Expiration値が含まれていない場合のデフォルトの有効期限間隔を指定します。

## プロパティ {#section-063be3b2f13a48a3a5ab8080718e9812}

0以上の実数。 応答データが生成されてから有効期限切れになるまでの時間数。 0に設定すると、常に応答イメージの有効期限が直ちに切れます。これにより、クライアントのキャッシュが事実上無効になります。 -1に設定すると、としてマークされま `never expire`す。

## 初期設定 {#section-f55308b195c04083996f6717c8537634}

定義されていな `default::Expiration` い場合や空の場合に継承されます。

TTL(Time-To-Live)は、キャッシュが期限切れになるまでの期間です。 デフォルトのTTLは10時間です。

## 関連項目 {#section-b2411d99ddb14115ad475d506efd8967}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
