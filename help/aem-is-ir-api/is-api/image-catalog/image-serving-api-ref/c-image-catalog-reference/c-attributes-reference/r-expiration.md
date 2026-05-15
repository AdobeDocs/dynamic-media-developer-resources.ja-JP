---
description: デフォルトのクライアントキャッシュの有効期間。 特定のカタログレコードに有効なカタログ有効期限の値が含まれていない場合に備えて、デフォルトの有効期限の間隔を指定します。
solution: Experience Manager
title: 有効期限
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9dccf8d-56b3-4608-ac05-9c17babc609e
TQID: 'https://experienceleague.adobe.com/NkQ-Bj-gHGksaD4Tmt7k8fYVEYfe67ACo4oWS25dKOE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 4%

---

# 有効期限{#expiration}

デフォルトのクライアントキャッシュの有効期間。 特定のカタログレコードに有効なcatalog::Expiration値が含まれていない場合に備えて、デフォルトの有効期限を指定します。

## プロパティ {#section-063be3b2f13a48a3a5ab8080718e9812}

実数、0以上。 返信データが生成されてから有効期限が切れるまでの時間数。 0に設定すると、返信画像が即座に期限切れになり、クライアントのキャッシュが効果的に無効になります。 `never expire`としてマークするには–1に設定します。

## 初期設定 {#section-f55308b195c04083996f6717c8537634}

定義されていない場合や空の場合は、`default::Expiration`から継承されます。

TTL （Time-To-Live）は、キャッシュの有効期限が切れるまでの時間です。 デフォルトのTTLは10時間です。

## 関連項目 {#section-b2411d99ddb14115ad475d506efd8967}

[ カタログ：：有効期限](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a)、[属性：:DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)、[属性：:NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
