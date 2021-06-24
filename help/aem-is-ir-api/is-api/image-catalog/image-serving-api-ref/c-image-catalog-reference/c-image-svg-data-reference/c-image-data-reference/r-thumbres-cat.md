---
description: サムネールの解像度 サムネール画像のオブジェクトの解像度を指定します。
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 1b462b7e-076d-433e-a5d2-e254396c4659
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 5%

---

# ThumbRes{#thumbres}

サムネールの解像度 サムネール画像のオブジェクトの解像度を指定します。

`catalog::ThumbType=3`の場合にのみ使用されます。

## プロパティ {#section-ee5cae086a3d4875805fa8a08756a586}

0より大きい実数値。 `catalog::Resolution`と同じ単位を持つ必要があります。

## 初期設定 {#section-f0e453fc8a7c451db21961c084eecabd}

`attribute::ThumbRes` が使用されるのは、フィールドが存在しない場合、値が0の場合、またはフィールドが空の場合です。

## 関連項目 {#section-eb716bf647614db083020fe8ce453751}

[catalog:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) 、 [catalog::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)、 [attribute::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501)、 [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、 [サムネールの拡大/縮小](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
