---
description: デフォルトの画像応答のクライアントキャッシュ TTL。 デフォルトの画像応答（defaultImage=または属性 DefaultImage で指定されたデフォルトの画像を返す応答）の有効期限を指定します。
solution: Experience Manager
title: DefaultExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 99103681-c00c-4648-8dee-2314e7e614af
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# DefaultExpiration{#defaultexpiration}

デフォルトの画像応答のクライアントキャッシュ TTL。 デフォルトの画像応答（defaultImage=または attribute::DefaultImage で指定されたデフォルトの画像を返す応答）の有効期限を指定します。

デフォルト画像がカタログレコードに関連付けられていない場合、またはデフォルト画像カタログレコードで特定の `catalog::Expiration` 値が提供されていない場合にのみ適用されます。

## プロパティ {#section-e564512476604fd7b964f9f2903d6d33}

0 以上の実数。 返信データが生成されてから有効期限が切れるまでの時間数。 常に返信画像をすぐに期限切れにする場合は 0 に設定します。これにより、デフォルトの画像応答のクライアントキャッシュが効果的に無効になります。 `-1` に設定すると、`never expire` としてマークされます。

## 初期設定 {#section-131cd32c2e214391857dba5af321f8cd}

定義されていない場合または空の場合は `default::DefaultExpiration` から継承します。

TTL （Time-To-Live）は、キャッシュの有効期限が切れるまでの期間です。 デフォルト TTL は 1 時間です。

## 関連項目 {#section-d8642c22e3d947129367dd76366963d6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a)、[attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
