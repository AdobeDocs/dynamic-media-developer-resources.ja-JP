---
description: CMYK初期設定の入力カラープロファイル カラー画像を埋め込まないCMYKソースプロファイルや、色=などの様々なプロファイルサービングコマンドで指定された特定のCMYKカラー値に使用するICCカラー画像の名前を指定します。
seo-description: CMYK初期設定の入力カラープロファイル カラー画像を埋め込まないCMYKソースプロファイルや、色=などの様々なプロファイルサービングコマンドで指定された特定のCMYKカラー値に使用するICCカラー画像の名前を指定します。
seo-title: IccProfileSrcCmyk
solution: Experience Manager
title: IccProfileSrcCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: 5f1c2eb6-7f32-4603-9587-d8c1f6a72bb0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK初期設定の入力カラープロファイル カラー画像を埋め込まないCMYKソースプロファイルや、色=などの様々なプロファイルサービングコマンドで指定された特定のCMYKカラー値に使用するICCカラー画像の名前を指定します。

## プロパティ {#section-fc2ad12a3c6e4c7cab495f1878638e66}

テキスト文字列。 指定する場合、この画像カタログまたは初期設定のカタログのICCプロファイルマップの有効な`icc::Name`値、または`attribute::RootPath`を基準とするファイルパスである必要があります。 参照先のICCプロファイルはCMYKプロファイルである必要があります。

## 初期設定 {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

定義されていない場合や空の場合は`default::IccProfileSrcCmyk`から継承されます。 `attribute::IccProfileSrcCmyk`が有効なプロファイルに解決されない場合は、代わりに`attribute::IccProfileCmyk`が使用されます。

## 関連項目 {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
