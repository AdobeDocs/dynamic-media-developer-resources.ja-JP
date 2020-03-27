---
description: サムネールの解像度 サムネール画像のオブジェクト解像度を指定します。
seo-description: サムネールの解像度 サムネール画像のオブジェクト解像度を指定します。
seo-title: ThumbRes
solution: Experience Manager
title: ThumbRes
topic: Scene7 Image Serving - Image Rendering API
uuid: 10bbad31-a0fd-4ed3-b708-87822777acdd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ThumbRes{#thumbres}

サムネールの解像度 サムネール画像のオブジェクト解像度を指定します。

使用されるのは、次の場合のみで `catalog::ThumbType=3`す。

## プロパティ {#section-ee5cae086a3d4875805fa8a08756a586}

0より大きい実数値。 と同じ単位を持つ必要がありま `catalog::Resolution`す。

## 初期設定 {#section-f0e453fc8a7c451db21961c084eecabd}

`attribute::ThumbRes` は、フィールドが存在しない場合、値が0の場合、またはフィールドが空の場合に使用されます。

## 関連項目 {#section-eb716bf647614db083020fe8ce453751}

[catalog:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) , [catalog::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1), [attribute:ThumbSumbReq](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501), [req=res](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)[, thumbnail Scaling](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
