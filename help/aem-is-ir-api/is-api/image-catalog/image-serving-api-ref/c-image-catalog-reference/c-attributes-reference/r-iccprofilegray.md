---
description: グレースケールの初期設定の出力カラープロファイル icc=で出力カラースペースが指定されていない場合にグレースケール応答画像に使用するICCカラープロファイルの名前を指定します。また、color=などの各種画像サービングコマンドで指定された特定のグレースケールカラー値も指定します。
solution: Experience Manager
title: IccProfileGray
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 2%

---


# IccProfileGray{#iccprofilegray}

グレースケールの初期設定の出力カラープロファイル icc=で出力カラースペースが指定されていない場合にグレースケール応答画像に使用するICCカラープロファイルの名前を指定します。また、color=などの各種画像サービングコマンドで指定された特定のグレースケールカラー値も指定します。

## プロパティ {#section-03f090ee2acf4537b83f78840d23ecab}

テキスト文字列。 指定する場合、この画像カタログまたは初期設定のカタログのICCプロファイルマップの有効な`icc::Name`値、または`attribute::RootPath`を基準とするファイルパスである必要があります。 参照先のICCプロファイルは、グレースケールプロファイルである必要があります。

## 初期設定 {#section-95ba3ab15edc4259b657c6ebf8783d61}

定義されていない場合や空の場合は`default::IccProfileGray`から継承されます。

## 関連項目 {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
