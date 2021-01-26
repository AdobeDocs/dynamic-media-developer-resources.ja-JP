---
description: RGB初期設定の出力カラープロファイル icc=で出力カラースペースが指定されていない場合にRGB応答画像に使用するICCカラープロファイルの名前を指定します。また、color=などの様々な画像サービングコマンドで指定された特定のRGBカラー値に使用します。
seo-description: RGB初期設定の出力カラープロファイル icc=で出力カラースペースが指定されていない場合にRGB応答画像に使用するICCカラープロファイルの名前を指定します。また、color=などの様々な画像サービングコマンドで指定された特定のRGBカラー値に使用します。
seo-title: IccProfileRgb
solution: Experience Manager
title: IccProfileRgb
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 40606151-d5fa-4ae5-b6f0-e811bfea4691
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---


# IccProfileRgb{#iccprofilergb}

RGB初期設定の出力カラープロファイル icc=で出力カラースペースが指定されていない場合にRGB応答画像に使用するICCカラープロファイルの名前を指定します。また、color=などの様々な画像サービングコマンドで指定された特定のRGBカラー値に使用します。

## プロパティ {#section-3dd55c954d4d4ad4bb715ed7cee31025}

テキスト文字列。 指定する場合、この画像カタログまたは初期設定のカタログのICCプロファイルマップの有効な`icc::Name`値、または`attribute::RootPath`を基準とするファイルパスである必要があります。 参照先のICCプロファイルはRGBプロファイルである必要があります。

## 初期設定 {#section-dfe08dd7b851453ca816623a4179955b}

定義されていない場合や空の場合は`default::IccProfileRgb`から継承されます。

## 関連項目 {#section-05bc25ab7caa418ca94d43ced905add7}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
