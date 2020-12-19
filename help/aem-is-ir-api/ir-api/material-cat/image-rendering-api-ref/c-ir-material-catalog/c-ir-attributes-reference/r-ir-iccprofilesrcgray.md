---
description: グレースケールの初期設定の入力カラープロファイル カラープロファイルを埋め込まないグレースケールマテリアルプロファイルに使用するICCカラー画像の名前を指定します。
seo-description: グレースケールの初期設定の入力カラープロファイル カラープロファイルを埋め込まないグレースケールマテリアルプロファイルに使用するICCカラー画像の名前を指定します。
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
topic: Scene7 Image Serving - Image Rendering API
uuid: e05d1185-ffd6-4c04-a2b8-52228beae37d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 2%

---


# IccProfileSrcGray{#iccprofilesrcgray}

グレースケールの初期設定の入力カラープロファイル カラープロファイルを埋め込まないグレースケールマテリアルプロファイルに使用するICCカラー画像の名前を指定します。

## プロパティ {#section-97923d8561b845309442d57d017d91a4}

テキスト文字列。 指定する場合、この画像カタログまたは初期設定のカタログのICCプロファイルマップの有効な`icc::Name`値、または`attribute::RootPath`を基準とするファイルパスである必要があります。 参照先のICCプロファイルは、グレースケールプロファイルである必要があります。

## 初期設定 {#section-02c52805ee13483dba7878aeab51f889}

定義されていない場合や空の場合は`default::IccProfileSrcGray`から継承されます。 `attribute::IccProfileSrcGray`が有効なプロファイルに解決されない場合は、代わりに`attribute::IccProfileGray`が使用されます。

## 関連項目 {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
