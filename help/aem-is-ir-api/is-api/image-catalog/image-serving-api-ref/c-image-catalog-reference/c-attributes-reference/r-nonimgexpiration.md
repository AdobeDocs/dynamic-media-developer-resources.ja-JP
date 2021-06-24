---
description: 非画像応答のクライアントキャッシュのTTL。 画像以外の特定の応答の有効期限間隔を指定します。
solution: Experience Manager
title: NonImgExpiration
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: c61e2781-dfaa-4f3d-958d-5ffa755a3e4d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---

# NonImgExpiration{#nonimgexpiration}

非画像応答のクライアントキャッシュのTTL。 画像以外の特定の応答の有効期限間隔を指定します。

次のコマンドに応じて送信される画像以外の特定の応答の有効期限を示します。

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## プロパティ {#section-d37e3113f4b1468b86b5a14e80d94c83}

0以上の実数。 応答データが生成されてから有効期限が切れるまでの時間数。 常に返信画像の有効期限を即座に切れるようにするには、0に設定します。これにより、デフォルトの画像応答のクライアントキャッシュが効果的に無効になります。 -1に設定すると、*無期限*&#x200B;とマークされます。

## 初期設定 {#section-96981360c0234b7f824d2ff7c25a7954}

`default::NonImgExpiration`から継承されます（定義されていない場合または空の場合）。

TTL(Time-To-Live)は、キャッシュが期限切れになるまでの期間です。 デフォルトのTTLは6分です。

## 関連項目 {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) 、 [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
