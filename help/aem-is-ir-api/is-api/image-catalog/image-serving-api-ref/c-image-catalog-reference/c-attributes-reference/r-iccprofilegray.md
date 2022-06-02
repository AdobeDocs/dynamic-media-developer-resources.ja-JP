---
title: IccProfileGray
description: グレースケールのデフォルト出力カラープロファイル。 icc=で出力カラースペースが指定されていない場合、および color=などの各種画像サービングコマンドで指定された特定のグレースケールカラー値に対して、グレースケール応答画像に使用する ICC カラープロファイルの名前を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4964c3b3-799d-40cb-bc5f-d08acfd41ed9
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---

# IccProfileGray{#iccprofilegray}

グレースケールのデフォルト出力カラープロファイル。 icc=で出力カラースペースが指定されていない場合、および color=などの各種画像サービングコマンドで指定された特定のグレースケールカラー値に対して、グレースケール応答画像に使用する ICC カラープロファイルの名前を指定します。

## プロパティ {#section-03f090ee2acf4537b83f78840d23ecab}

テキスト文字列。 指定する場合、有効な `icc::Name` この画像カタログまたはデフォルトカタログの ICC プロファイルマップからの値、または `attribute::RootPath`. 参照する ICC プロファイルは、グレースケールプロファイルである必要があります。

## 初期設定 {#section-95ba3ab15edc4259b657c6ebf8783d61}

継承元 `default::IccProfileGray` が定義されていない場合、または空の場合は。

## 関連項目 {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
