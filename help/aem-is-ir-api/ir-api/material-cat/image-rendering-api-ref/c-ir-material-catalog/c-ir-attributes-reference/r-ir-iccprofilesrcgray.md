---
description: グレースケールの初期設定の入力カラープロファイル カラープロファイルを埋め込まないグレースケールマテリアルプロファイルに使用するICCカラー画像の名前を指定します。
solution: Experience Manager
title: IccProfileSrcGray
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '134'
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
