---
description: グレースケールのデフォルト出力カラープロファイル icc=で出力カラースペースが指定されていない場合にグレースケール応答画像に使用するICCカラープロファイルの名前を指定します。また、color=などの様々な画像サービングコマンドで指定された特定のグレースケールカラー値を指定します。
solution: Experience Manager
title: IccProfileGray
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 4964c3b3-799d-40cb-bc5f-d08acfd41ed9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---

# IccProfileGray{#iccprofilegray}

グレースケールのデフォルト出力カラープロファイル icc=で出力カラースペースが指定されていない場合にグレースケール応答画像に使用するICCカラープロファイルの名前を指定します。また、color=などの様々な画像サービングコマンドで指定された特定のグレースケールカラー値を指定します。

## プロパティ {#section-03f090ee2acf4537b83f78840d23ecab}

テキスト文字列。 指定する場合、この画像カタログまたはデフォルトカタログのICCプロファイルマップの有効な`icc::Name`値、または`attribute::RootPath`を基準とするファイルパスを指定する必要があります。 参照されるICCプロファイルは、グレースケールプロファイルである必要があります。

## 初期設定 {#section-95ba3ab15edc4259b657c6ebf8783d61}

`default::IccProfileGray`から継承されます（定義されていない場合または空の場合）。

## 関連項目 {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) 、 [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)、 [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)、 [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
