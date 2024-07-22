---
description: 非画像応答のクライアントキャッシュ TTL。 画像以外の特定の応答の有効期間を指定します。
solution: Experience Manager
title: NonImgExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c61e2781-dfaa-4f3d-958d-5ffa755a3e4d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# NonImgExpiration{#nonimgexpiration}

非画像応答のクライアントキャッシュ TTL。 画像以外の特定の応答の有効期間を指定します。

画像以外の特定の応答（次のコマンドに応答して送信される応答を含む）の有効期限の間隔を指定します。

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## プロパティ {#section-d37e3113f4b1468b86b5a14e80d94c83}

0 以上の実数。 返信データが生成されてから有効期限が切れるまでの時間数。 常に返信画像をすぐに期限切れにする場合は 0 に設定します。これにより、デフォルトの画像応答のクライアントキャッシュが効果的に無効になります。 -1 に設定すると、*有効期限切れになりません* としてマークされます。

## 初期設定 {#section-96981360c0234b7f824d2ff7c25a7954}

定義されていない場合または空の場合は `default::NonImgExpiration` から継承します。

TTL （Time-To-Live）は、キャッシュの有効期限が切れるまでの期間です。 デフォルト TTL は 6 分です。

## 関連項目 {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a)、[attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
