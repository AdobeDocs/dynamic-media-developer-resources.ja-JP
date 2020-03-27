---
description: グレースケールの初期設定の出力カラープロファイル icc=で出力カラースペースが指定されていない場合にグレースケール応答画像に使用するICCカラープロファイルの名前を指定し、color=などの様々な画像サービングコマンドで指定された特定のグレースケールカラー値を指定します。
seo-description: グレースケールの初期設定の出力カラープロファイル icc=で出力カラースペースが指定されていない場合にグレースケール応答画像に使用するICCカラープロファイルの名前を指定し、color=などの様々な画像サービングコマンドで指定された特定のグレースケールカラー値を指定します。
seo-title: IccProfileGray
solution: Experience Manager
title: IccProfileGray
topic: Scene7 Image Serving - Image Rendering API
uuid: a7d40114-f91f-4637-bb49-5b06b9ce846d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileGray{#iccprofilegray}

グレースケールの初期設定の出力カラープロファイル icc=で出力カラースペースが指定されていない場合にグレースケール応答画像に使用するICCカラープロファイルの名前を指定し、color=などの様々な画像サービングコマンドで指定された特定のグレースケールカラー値を指定します。

## プロパティ {#section-03f090ee2acf4537b83f78840d23ecab}

テキスト文字列。 指定する場合、この画像カタログま `icc::Name` たは初期設定のカタログのICCプロファイルマップ、またはを基準とする相対ファイルパスの有効な値である必要がありま `attribute::RootPath`す。 参照先のICCプロファイルは、グレースケールプロファイルである必要があります。

## 初期設定 {#section-95ba3ab15edc4259b657c6ebf8783d61}

定義されていな `default::IccProfileGray` い場合や空の場合に継承されます。

## 関連項目 {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
