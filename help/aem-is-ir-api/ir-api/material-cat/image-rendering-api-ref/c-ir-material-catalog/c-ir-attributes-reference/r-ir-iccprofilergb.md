---
description: RGBのデフォルト出力カラープロファイル icc=で出力カラースペースが指定されていない場合にRGB応答画像に使用するICCカラープロファイルの名前を指定します。また、bgc=やcolor=など、様々な画像レンダリングコマンドで指定された特定のRGBカラー値を指定します。
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 4057e968-24de-41af-9901-a6cb5ed9ea63
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---

# IccProfileRgb{#iccprofilergb}

RGBのデフォルト出力カラープロファイル icc=で出力カラースペースが指定されていない場合にRGB応答画像に使用するICCカラープロファイルの名前を指定します。また、bgc=やcolor=など、様々な画像レンダリングコマンドで指定された特定のRGBカラー値を指定します。

## プロパティ {#section-b4a1bd92e99047479a5036413525a6d9}

テキスト文字列。 指定する場合は、このマテリアルカタログまたはデフォルトカタログのICCプロファイルマップの有効な`icc::Name`値か、`attribute::RootPath`を基準とするファイルパスを指定する必要があります。 参照されるICCプロファイルは、RGBプロファイルである必要があります。

## 初期設定 {#section-5809772f8e96438ab7626d323c66a4ba}

`default::IccProfileRgb`から継承されます（定義されていない場合または空の場合）。

## 関連項目 {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) 、 [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)、 [attribute::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49)、 [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
