---
description: 初期設定の画像応答のクライアントキャッシュTTL。 初期設定の画像応答（defaultImage=または属性DefaultImageで指定された初期設定の画像を返す応答）の有効期限を指定します。
seo-description: 初期設定の画像応答のクライアントキャッシュTTL。 初期設定の画像応答（defaultImage=または属性DefaultImageで指定された初期設定の画像を返す応答）の有効期限を指定します。
seo-title: DefaultExpiration
solution: Experience Manager
title: DefaultExpiration
topic: Scene7 Image Serving - Image Rendering API
uuid: 5266bff9-f20b-4b3b-9566-8a3f5ba0777a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# DefaultExpiration{#defaultexpiration}

初期設定の画像応答のクライアントキャッシュTTL。 初期設定の画像応答（defaultImage=またはattribute::DefaultImageで指定された初期設定の画像を返す応答）の有効期限を指定します。

初期設定の画像がカタログレコードに関連付けられていない場合、または初期設定の画像カタログレコードで特定の`catalog::Expiration`値が指定されていない場合にのみ適用されます。

## プロパティ {#section-e564512476604fd7b964f9f2903d6d33}

0以上の実数。 応答データが生成されてから有効期限切れになるまでの時間数。 常に返信画像を即座に期限切れにする場合は0に設定します。これにより、デフォルトの画像応答のクライアントキャッシュが効果的に無効になります。 `-1`に設定して`never expire`とマークします。

## 初期設定 {#section-131cd32c2e214391857dba5af321f8cd}

定義されていない場合や空の場合は`default::DefaultExpiration`から継承されます。

TTL(Time-To-Live)は、キャッシュが期限切れになるまでの期間です。 デフォルトのTTLは1時間です。

## 関連項目 {#section-d8642c22e3d947129367dd76366963d6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
