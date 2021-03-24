---
description: RGB初期設定の出力カラープロファイル icc=で出力カラースペースが指定されていない場合にRGB応答画像に使用するICCカラープロファイルの名前を指定します。また、bgc=やcolor=などの各種の画像レンダリングコマンドで指定された特定のRGBカラー値も指定します。
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---


# IccProfileRgb{#iccprofilergb}

RGB初期設定の出力カラープロファイル icc=で出力カラースペースが指定されていない場合にRGB応答画像に使用するICCカラープロファイルの名前を指定します。また、bgc=やcolor=などの各種の画像レンダリングコマンドで指定された特定のRGBカラー値も指定します。

## プロパティ {#section-b4a1bd92e99047479a5036413525a6d9}

テキスト文字列。 指定する場合、このマテリアルカタログまたは初期設定のカタログのICCプロファイルマップ、または`attribute::RootPath`を基準とするファイルパスの有効な`icc::Name`値である必要があります。 参照先のICCプロファイルはRGBプロファイルである必要があります。

## 初期設定 {#section-5809772f8e96438ab7626d323c66a4ba}

定義されていない場合や空の場合は`default::IccProfileRgb`から継承されます。

## 関連項目 {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
