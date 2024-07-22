---
description: サムネールの水平方向の配置。 wid=および hei=で指定した、または DefaultThumbPix 属性で指定した返信画像の長方形内のサムネール画像の水平方向揃えを指定します。
solution: Experience Manager
title: ThumbHorizAlign
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a51f92a-ffb9-4460-a910-9f2fefe3eae5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# ThumbHorizAlign{#thumbhorizalign}

サムネールの水平方向の配置。 wid=および hei=または attribute::DefaultThumbPix で指定された返信画像の長方形内のサムネール画像の水平方向揃えを指定します。

サムネールリクエスト（`req=tmb`）にのみ使用されます。

## プロパティ {#section-c98f793986cd4f98a3995615e3b68f76}

列挙値。 左揃え、中央揃え、右揃えには、それぞれ 1、2、3 の値を使用できます。

## 初期設定 {#section-0c06f0d998cb4306868b360a06c32e5b}

定義されていない場合または空の場合は `default::ThumbHorizAlign` から継承します。

## 関連項目 {#section-a74a13c3643140cf971d7a4275e0fdb3}

[catalog::ThumbType](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03)、[attribute::DefaultThumbPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultthumbpix.md#reference-cf52bb74bed2466e8bc8adb0cacd6141)、[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)、[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
