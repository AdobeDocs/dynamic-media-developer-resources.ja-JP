---
description: CMYK のデフォルト出力カラープロファイル。 出力カラースペースが icc=で指定されていない場合や、様々な画像サービングコマンドで指定された特定の CMYK カラー値（color=など）に対して、CMYK 応答画像に使用する ICC カラープロファイルの名前を指定します。
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2bf83cf5-3fc9-42aa-a143-4b56e43ee4d1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---

# IccProfileCmyk{#iccprofilecmyk}

CMYK のデフォルト出力カラープロファイル。 出力カラースペースが icc=で指定されていない場合や、様々な画像サービングコマンドで指定された特定の CMYK カラー値（color=など）に対して、CMYK 応答画像に使用する ICC カラープロファイルの名前を指定します。

## プロパティ {#section-d8b6102cc1c744d482f99808ccfcaa24}

テキスト文字列 指定する場合、は、この画像カタログまたはデフォルトのカタログの ICC プロファイルマップの有効な `icc::Name` 値、または `attribute::RootPath` に対する相対ファイルパスである必要があります。 参照される ICC プロファイルは、CMYK プロファイルである必要があります。

## 初期設定 {#section-62442df09a724950bfbdd0640b3e6678}

定義されていない場合または空の場合は `default::IccProfileCmyk` から継承します。

## 関連項目 {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe)、[attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)、[attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)、[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
