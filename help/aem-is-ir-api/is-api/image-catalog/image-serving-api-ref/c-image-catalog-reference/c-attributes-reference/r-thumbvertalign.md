---
description: サムネールの垂直方向の整列。 wid=および hei=で指定した、または DefaultThumbPix 属性で指定した返信画像の長方形内のサムネール画像の垂直方向揃えを指定します。
solution: Experience Manager
title: ThumbVertAlign
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bb1aa398-5638-4109-bf05-bc51ace4146d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# ThumbVertAlign{#thumbvertalign}

サムネールの垂直方向の整列。 wid=および hei=または attribute::DefaultThumbPix で指定された返信画像の長方形内のサムネール画像の垂直方向揃えを指定します。

サムネールリクエスト（`req=tmb`）にのみ使用されます。

## プロパティ {#section-f02c23248e87419caf3d95add51aea1e}

列挙値。 上揃え、中央揃え、下揃えには、それぞれ 1、2、3 の値を使用できます。

## 初期設定 {#section-30caa4e772254419ad7a3a89d440666c}

定義されていない場合または空の場合は `default::ThumbHorizAlign` から継承します。

## 関連項目 {#section-c4cd5209d994498eb56a78fcd5bbdfa4}

[catalog::ThumbType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md)、[attribute::DefaultThumbPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultthumbpix.md#reference-cf52bb74bed2466e8bc8adb0cacd6141)、[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)、[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
