---
description: CMYK初期設定の出力カラープロファイル icc=で出力カラースペースが指定されていない場合にCMYK応答画像に使用するICCカラープロファイルの名前を指定します。また、color=などの様々な画像サービングコマンドで指定された特定のCMYKカラー値も指定します。
seo-description: CMYK初期設定の出力カラープロファイル icc=で出力カラースペースが指定されていない場合にCMYK応答画像に使用するICCカラープロファイルの名前を指定します。また、color=などの様々な画像サービングコマンドで指定された特定のCMYKカラー値も指定します。
seo-title: IccProfileCmyk
solution: Experience Manager
title: IccProfileCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: b22b6ed1-615f-4241-b4d4-c3aa70351458
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---


# IccProfileCmyk{#iccprofilecmyk}

CMYK初期設定の出力カラープロファイル icc=で出力カラースペースが指定されていない場合にCMYK応答画像に使用するICCカラープロファイルの名前を指定します。また、color=などの様々な画像サービングコマンドで指定された特定のCMYKカラー値も指定します。

## プロパティ {#section-d8b6102cc1c744d482f99808ccfcaa24}

テキスト文字列。 指定する場合、この画像カタログまたは初期設定のカタログのICCプロファイルマップの有効な`icc::Name`値、または`attribute::RootPath`を基準とするファイルパスである必要があります。 参照先のICCプロファイルはCMYKプロファイルである必要があります。

## 初期設定 {#section-62442df09a724950bfbdd0640b3e6678}

定義されていない場合や空の場合は`default::IccProfileCmyk`から継承されます。

## 関連項目 {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
