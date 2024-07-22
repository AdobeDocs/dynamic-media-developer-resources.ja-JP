---
title: IccProfileSrcCmyk
description: CMYK のデフォルト入力カラープロファイル。 カラープロファイルを埋め込まない CMYK ソース画像と、様々な画像サービングコマンドで指定された特定の CMYK カラー値（color=など）に使用する ICC カラープロファイルの名前を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 018170f3-2d1a-4da1-a480-b0a7e19457d8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK のデフォルト入力カラープロファイル。 カラープロファイルを埋め込まない CMYK ソース画像と、様々な画像サービングコマンドで指定された特定の CMYK カラー値（color=など）に使用する ICC カラープロファイルの名前を指定します。

## プロパティ {#section-fc2ad12a3c6e4c7cab495f1878638e66}

テキスト文字列 指定する場合、は、この画像カタログまたはデフォルトのカタログの ICC プロファイルマップの有効な `icc::Name` 値、または `attribute::RootPath` に対する相対ファイルパスである必要があります。 参照される ICC プロファイルは、CMYK プロファイルである必要があります。

## 初期設定 {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

定義されていない場合または空の場合は `default::IccProfileSrcCmyk` から継承します。 `attribute::IccProfileSrcCmyk` が有効なプロファイルに解決されない場合は、代わりに `attribute::IccProfileCmyk` が使用されます。

## 関連項目 {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe)、[attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)、[attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)、[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
