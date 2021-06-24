---
description: デフォルトの画像応答のクライアントキャッシュTTL。 デフォルトの画像応答の有効期限間隔を指定します（応答は、 defaultImage=または属性DefaultImageで指定されたデフォルトの画像を返します）。
solution: Experience Manager
title: DefaultExpiration
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 99103681-c00c-4648-8dee-2314e7e614af
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---

# DefaultExpiration{#defaultexpiration}

デフォルトの画像応答のクライアントキャッシュTTL。 デフォルトの画像応答の有効期限を指定します（応答は、 defaultImage=またはattribute::DefaultImageで指定されたデフォルトの画像を返します）。

デフォルトの画像がカタログレコードに関連付けられていない場合、またはデフォルトの画像カタログレコードに特定の`catalog::Expiration`値が指定されていない場合にのみ適用されます。

## プロパティ {#section-e564512476604fd7b964f9f2903d6d33}

0以上の実数。 応答データが生成されてから有効期限が切れるまでの時間数。 常に返信画像の有効期限を即座に切れるようにするには、0に設定します。これにより、デフォルトの画像応答のクライアントキャッシュが効果的に無効になります。 `-1`に設定すると、`never expire`としてマークされます。

## 初期設定 {#section-131cd32c2e214391857dba5af321f8cd}

`default::DefaultExpiration`から継承されます（定義されていない場合または空の場合）。

TTL(Time-To-Live)は、キャッシュが期限切れになるまでの期間です。 デフォルトのTTLは1時間です。

## 関連項目 {#section-d8642c22e3d947129367dd76366963d6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) 、 [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
