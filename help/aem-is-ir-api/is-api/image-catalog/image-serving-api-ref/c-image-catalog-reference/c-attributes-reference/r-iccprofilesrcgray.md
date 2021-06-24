---
description: グレースケールのデフォルト入力カラープロファイル カラープロファイルを埋め込まないグレースケールソース画像や、color=などの様々な画像サービングコマンドで指定された特定のグレースケールカラー値に使用するICCカラープロファイルの名前を指定します。
solution: Experience Manager
title: IccProfileSrcGray
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 54290f71-36b2-4b37-ac04-4fe85c1f34ab
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---

# IccProfileSrcGray{#iccprofilesrcgray}

グレースケールのデフォルト入力カラープロファイル カラープロファイルを埋め込まないグレースケールソース画像や、color=などの様々な画像サービングコマンドで指定された特定のグレースケールカラー値に使用するICCカラープロファイルの名前を指定します。

## プロパティ {#section-8cbb316df6eb463aaca7b308d3568086}

テキスト文字列。 指定する場合、この画像カタログまたはデフォルトカタログのICCプロファイルマップの有効な`icc::Name`値、または`attribute::RootPath`を基準とするファイルパスを指定する必要があります。 参照されるICCプロファイルは、グレースケールプロファイルである必要があります。

## 初期設定 {#section-bcc7250715884412bd0780f60d1cce7b}

`default::IccProfileSrcGray`から継承されます（定義されていない場合または空の場合）。 `attribute::IccProfileSrcGray`が有効なプロファイルに解決されない場合は、代わりに`attribute::IccProfileGray`が使用されます。

## 関連項目 {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) 、 [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)、 [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)、 [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
