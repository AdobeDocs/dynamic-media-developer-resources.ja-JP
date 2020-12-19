---
description: RGB初期設定の入力カラープロファイル カラー画像を埋め込まないRGBソースプロファイルや、色=などの様々なプロファイルサービングコマンドで指定された特定のRGBカラー値に使用するICCカラー画像の名前を指定します。
seo-description: RGB初期設定の入力カラープロファイル カラー画像を埋め込まないRGBソースプロファイルや、色=などの様々なプロファイルサービングコマンドで指定された特定のRGBカラー値に使用するICCカラー画像の名前を指定します。
seo-title: IccProfileSrcRgb
solution: Experience Manager
title: IccProfileSrcRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 4f6f19ec-3524-403e-9c79-1e2b25cd74ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB初期設定の入力カラープロファイル カラー画像を埋め込まないRGBソースプロファイルや、色=などの様々なプロファイルサービングコマンドで指定された特定のRGBカラー値に使用するICCカラー画像の名前を指定します。

## プロパティ {#section-3cd753196959462e9e674dab0b033d08}

テキスト文字列。 指定する場合、この画像カタログまたは初期設定のカタログのICCプロファイルマップの有効な`icc::Name`値、または`attribute::RootPath`を基準とするファイルパスである必要があります。 参照先のICCプロファイルはRGBプロファイルである必要があります。

## 初期設定 {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

定義されていない場合や空の場合は`default::IccProfileSrcRgb`から継承されます。 `attribute::IccProfileSrcRgb`が有効なプロファイルに解決されない場合は、代わりに`attribute::IccProfileRgb`が使用されます。

## 関連項目 {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
