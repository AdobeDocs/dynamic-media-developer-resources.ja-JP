---
description: 画像以外の応答のクライアントキャッシュTTL。 画像以外の特定の応答の有効期限の間隔を指定します。
seo-description: 画像以外の応答のクライアントキャッシュTTL。 画像以外の特定の応答の有効期限の間隔を指定します。
seo-title: NonImgExpiration
solution: Experience Manager
title: NonImgExpiration
topic: Scene7 Image Serving - Image Rendering API
uuid: 19b37bd4-f7cf-4b5f-be1a-b2d9fda5b4b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# NonImgExpiration{#nonimgexpiration}

画像以外の応答のクライアントキャッシュTTL。 画像以外の特定の応答の有効期限の間隔を指定します。

次のコマンドに応答して送信される応答を含む、特定の非画像応答の有効期限間隔を指定します。

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## プロパティ {#section-d37e3113f4b1468b86b5a14e80d94c83}

0以上の実数。 応答データが生成されてから有効期限切れになるまでの時間数。 常に返信画像を即座に期限切れにする場合は0に設定します。これにより、デフォルトの画像応答のクライアントキャッシュが効果的に無効になります。 *never expire*&#x200B;とマークするには、-1に設定します。

## 初期設定 {#section-96981360c0234b7f824d2ff7c25a7954}

定義されていない場合や空の場合は`default::NonImgExpiration`から継承されます。

TTL(Time-To-Live)は、キャッシュが期限切れになるまでの期間です。 デフォルトのTTLは6分です。

## 関連項目 {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
