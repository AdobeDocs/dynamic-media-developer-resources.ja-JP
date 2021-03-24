---
description: サムネールの初期設定の背景色。 出力サムネール画像の、実際の画像データを含まない領域の塗りつぶしに使用されるRGB値。
solution: Experience Manager
title: ThumbBkgColor
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 5%

---


# ThumbBkgColor{#thumbbkgcolor}

サムネールの初期設定の背景色。 出力サムネール画像の、実際の画像データを含まない領域の塗りつぶしに使用されるRGB値。

サムネール要求(`req=tmb`)および`catalog::ThumbType`が2または3に設定されている場合にのみ使用されます。

## プロパティ {#section-a73e82c950cc4319bc3bccec14764c25}

カラー.

## 初期設定 {#section-b02bb56dda684ff9969806ce82ba00c2}

定義されていない場合や空の場合は`default::ThumbBkgColor`から継承されます。

## 関連項目 {#section-27983dc885424dfbba8c8e4192f3f88d}

[catalog::ThumbType](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) 、 [req=tmb](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
