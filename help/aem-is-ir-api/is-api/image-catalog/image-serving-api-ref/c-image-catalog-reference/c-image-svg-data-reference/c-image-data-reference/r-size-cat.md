---
description: 画像サイズ。 カタログパスが参照する高解像度の画像のピクセルサイズ。
solution: Experience Manager
title: サイズ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f06cbb-d70f-4334-966c-624b49c3bb9b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 5%

---

# サイズ{#size}

画像サイズ。 catalog::Path が参照するフル解像度画像のピクセルサイズ。

この値が指定されている場合、画像サービングではこの値を使用して、実際の画像サイズを取得するために画像を開く必要がなくなります。

>[!NOTE]
>
>`catalog::Size` が指定され、実際のフル解像度の画像サイズと同じでない場合は、動作が未定義になる可能性があります。

## プロパティ {#section-5c914ec8b1444a8e99d811b647cd42a3}

0 より大きい 2 つの整数。コンマで区切ります。 オプション。

## 初期設定 {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

フィールドが存在しない場合やフィールドが空の場合は、画像の実際のサイズが使用されます。

## 関連項目 {#section-e63797357d5a4119a10db1e6e088f6e9}

[catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) , [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
