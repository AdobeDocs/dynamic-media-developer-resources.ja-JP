---
description: 非イメージ応答のクライアント キャッシュ TTL。 特定の画像以外の応答の有効期限を指定します。
solution: Experience Manager
title: NonImgExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c61e2781-dfaa-4f3d-958d-5ffa755a3e4d
TQID: 'https://experienceleague.adobe.com/A21KkwsYFIMp9Pw0WyX-c-3UVlFg2FacObh2jjRVTwA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 128
ht-degree: 2%

---

# NonImgExpiration{#nonimgexpiration}

非イメージ応答のクライアント キャッシュ TTL。 特定の画像以外の応答の有効期限を指定します。

次のコマンドに対する応答を含む、特定の画像以外の応答の有効期限を示します。

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## プロパティ {#section-d37e3113f4b1468b86b5a14e80d94c83}

実数、0以上。 返信データが生成されてから有効期限が切れるまでの時間数。 0に設定すると、返信画像が即座に期限切れになり、デフォルトの画像応答のクライアントキャッシュが効果的に無効になります。 *有効期限なし*&#x200B;としてマークするには、-1に設定します。

## 初期設定 {#section-96981360c0234b7f824d2ff7c25a7954}

定義されていない場合や空の場合は、`default::NonImgExpiration`から継承されます。

TTL （Time-To-Live）は、キャッシュの有効期限が切れるまでの時間です。 デフォルト TTLは6分です。

## 関連項目 {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[ カタログ：：有効期限](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a)、[属性：:DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
