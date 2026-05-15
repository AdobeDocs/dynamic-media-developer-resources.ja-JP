---
description: サムネール解決： サムネール画像のオブジェクト解像度を指定します。
solution: Experience Manager
title: サムレス
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b462b7e-076d-433e-a5d2-e254396c4659
TQID: 'https://experienceleague.adobe.com/A7vuk3uRPTC-EUgmh4OhVHYYA4BThHxD0vMnB3yw1Bs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 69
ht-degree: 4%

---

# サムレス{#thumbres}

サムネール解決： サムネール画像のオブジェクト解像度を指定します。

`catalog::ThumbType=3`の場合にのみ使用されます。

## プロパティ {#section-ee5cae086a3d4875805fa8a08756a586}

実数値の値が0より大きい。 `catalog::Resolution`と同じ単位が必要です。

## 初期設定 {#section-f0e453fc8a7c451db21961c084eecabd}

`attribute::ThumbRes`は、フィールドが存在しない場合、値が0の場合、またはフィールドが空の場合に使用されます。

## 関連項目 {#section-eb716bf647614db083020fe8ce453751}

[ カタログ :ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03)、[ カタログ：：解像度](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)、[属性：:ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501)、[req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、[ サムネール拡大・縮小](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
