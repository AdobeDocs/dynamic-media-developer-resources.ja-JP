---
description: グレースケールの初期設定の入力カラープロファイル カラー画像を埋め込まないグレースケールソースプロファイルや、color=などの各種画像サービングコマンドで指定された特定のグレースケールカラー値に使用するICCカラープロファイルの名前を指定します。
seo-description: グレースケールの初期設定の入力カラープロファイル カラー画像を埋め込まないグレースケールソースプロファイルや、color=などの各種画像サービングコマンドで指定された特定のグレースケールカラー値に使用するICCカラープロファイルの名前を指定します。
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
topic: Scene7 Image Serving - Image Rendering API
uuid: 823c0e33-8bb7-4754-81cf-61a5ed6f45ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---


# IccProfileSrcGray{#iccprofilesrcgray}

グレースケールの初期設定の入力カラープロファイル カラー画像を埋め込まないグレースケールソースプロファイルや、color=などの各種画像サービングコマンドで指定された特定のグレースケールカラー値に使用するICCカラープロファイルの名前を指定します。

## プロパティ {#section-8cbb316df6eb463aaca7b308d3568086}

テキスト文字列。 指定する場合、この画像カタログまたは初期設定のカタログのICCプロファイルマップの有効な`icc::Name`値、または`attribute::RootPath`を基準とするファイルパスである必要があります。 参照先のICCプロファイルは、グレースケールプロファイルである必要があります。

## 初期設定 {#section-bcc7250715884412bd0780f60d1cce7b}

定義されていない場合や空の場合は`default::IccProfileSrcGray`から継承されます。 `attribute::IccProfileSrcGray`が有効なプロファイルに解決されない場合は、代わりに`attribute::IccProfileGray`が使用されます。

## 関連項目 {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
