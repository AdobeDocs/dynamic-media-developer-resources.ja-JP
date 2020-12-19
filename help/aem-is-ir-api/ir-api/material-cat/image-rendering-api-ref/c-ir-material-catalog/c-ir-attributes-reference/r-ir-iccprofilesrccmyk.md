---
description: CMYK初期設定の入力カラープロファイル カラープロファイルを埋め込まないCMYKマテリアルプロファイルに使用するICCカラー画像の名前を指定します。
seo-description: CMYK初期設定の入力カラープロファイル カラープロファイルを埋め込まないCMYKマテリアルプロファイルに使用するICCカラー画像の名前を指定します。
seo-title: IccProfileSrcCmyk
solution: Experience Manager
title: IccProfileSrcCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: 95147b28-c87b-4337-a0eb-a962ca1e8786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 2%

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK初期設定の入力カラープロファイル カラープロファイルを埋め込まないCMYKマテリアルプロファイルに使用するICCカラー画像の名前を指定します。

## プロパティ {#section-0cee77438d914c319ec876edb3490821}

テキスト文字列。 指定する場合、この画像カタログまたは初期設定のカタログのICCプロファイルマップの有効な`icc::Name`値、または`attribute::RootPath`を基準とするファイルパスである必要があります。 参照先のICCプロファイルはCMYKプロファイルである必要があります。

## 初期設定 {#section-11f6239e0dd14827abf4a95c1b30161c}

定義されていない場合や空の場合は`default::IccProfileSrcCmyk`から継承されます。 `attribute::IccProfileSrcCmyk`が有効なプロファイルに解決されない場合は、代わりに`attribute::IccProfileCmyk`が使用されます。

## 関連項目 {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
