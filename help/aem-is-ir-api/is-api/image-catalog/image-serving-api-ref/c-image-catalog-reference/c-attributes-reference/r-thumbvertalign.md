---
description: サムネールの垂直方向の配置。 wid=とhei=で指定した返信画像の長方形または属性DefaultThumbPixで指定した返信画像の中のサムネール画像の垂直方向の位置を指定します。
solution: Experience Manager
title: ThumbVertAlign
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---


# ThumbVertAlign{#thumbvertalign}

サムネールの垂直方向の配置。 wid=およびhei=またはattribute::DefaultThumbPixで指定した返信画像の長方形内でのサムネール画像の垂直方向の位置を指定します。

サムネール要求(`req=tmb`)にのみ使用されます。

## プロパティ {#section-f02c23248e87419caf3d95add51aea1e}

列挙。 許可される値は、上揃え、中央揃え、下揃えのそれぞれに1、2、3です。

## 初期設定 {#section-30caa4e772254419ad7a3a89d440666c}

定義されていない場合や空の場合は`default::ThumbHorizAlign`から継承されます。

## 関連項目 {#section-c4cd5209d994498eb56a78fcd5bbdfa4}

[catalog::ThumbType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md) ,  [attribute::DefaultThumbPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultthumbpix.md#reference-cf52bb74bed2466e8bc8adb0cacd6141),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47),  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
