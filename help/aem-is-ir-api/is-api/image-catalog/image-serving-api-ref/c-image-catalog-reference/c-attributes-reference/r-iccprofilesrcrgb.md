---
description: RGBのデフォルト入力カラープロファイル。 カラープロファイルを埋め込まないRGB ソース画像および様々な画像サービングコマンドで指定された特定のRGB カラー値（color=など）に使用する ICC カラープロファイルの名前を指定します。
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfcbd9fe-e696-46e3-abbf-497dc55fe855
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

RGBのデフォルト入力カラープロファイル。 カラープロファイルを埋め込まないRGB ソース画像および様々な画像サービングコマンドで指定された特定のRGB カラー値（color=など）に使用する ICC カラープロファイルの名前を指定します。

## プロパティ {#section-3cd753196959462e9e674dab0b033d08}

テキスト文字列 指定する場合、は、この画像カタログまたはデフォルトのカタログの ICC プロファイルマップの有効な `icc::Name` 値、または `attribute::RootPath` に対する相対ファイルパスである必要があります。 参照される ICC プロファイルは、RGB プロファイルである必要があります。

## 初期設定 {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

定義されていない場合または空の場合は `default::IccProfileSrcRgb` から継承します。 `attribute::IccProfileSrcRgb` が有効なプロファイルに解決されない場合は、代わりに `attribute::IccProfileRgb` が使用されます。

## 関連項目 {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe)、[attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)、[attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)、[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
