---
description: 画像サイズ. カタログパスで参照される最大解像度の画像のピクセルサイズ。
seo-description: 画像サイズ. カタログパスで参照される最大解像度の画像のピクセルサイズ。
seo-title: サイズ
solution: Experience Manager
title: サイズ
topic: Scene7 Image Serving - Image Rendering API
uuid: 6fe2aeb6-0dd7-4631-955f-ad74d11b613d
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# サイズ{#size}

画像サイズ. catalog::Pathで参照される最大解像度画像のピクセルサイズ。

この値を指定すると、画像サービングはこの値を使用して、実際の画像サイズを取得するために画像を開く必要がなくなります。

>[!NOTE]
>
>を指 `catalog::Size`定し、実際の最大解像度の画像サイズと異なる場合、未定義の動作が発生する可能性があります。

## プロパティ {#section-5c914ec8b1444a8e99d811b647cd42a3}

それぞれが0より大きい2つの整数で、コンマで区切られます。 （オプション）

## 初期設定 {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

フィールドが存在しない場合、またはフィールドが空の場合は、画像の実際のサイズが使用されます。

## 関連項目 {#section-e63797357d5a4119a10db1e6e088f6e9}

[catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) , [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
