---
description: RGBのデフォルト出力カラープロファイル icc=で出力カラースペースが指定されていない場合にRGB応答画像に使用するICCカラープロファイルの名前を指定します。また、color=などの様々な画像サービングコマンドで指定された特定のRGBカラー値を指定します。
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 861c7b54-6d18-47c8-a08d-970f29b63962
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---

# IccProfileRgb{#iccprofilergb}

RGBのデフォルト出力カラープロファイル icc=で出力カラースペースが指定されていない場合にRGB応答画像に使用するICCカラープロファイルの名前を指定します。また、color=などの様々な画像サービングコマンドで指定された特定のRGBカラー値を指定します。

## プロパティ {#section-3dd55c954d4d4ad4bb715ed7cee31025}

テキスト文字列。 指定する場合、この画像カタログまたはデフォルトカタログのICCプロファイルマップの有効な`icc::Name`値、または`attribute::RootPath`を基準とするファイルパスを指定する必要があります。 参照されるICCプロファイルは、RGBプロファイルである必要があります。

## 初期設定 {#section-dfe08dd7b851453ca816623a4179955b}

`default::IccProfileRgb`から継承されます（定義されていない場合または空の場合）。

## 関連項目 {#section-05bc25ab7caa418ca94d43ced905add7}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) 、 [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)、 [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)、 [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
