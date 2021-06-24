---
description: RGBの初期設定の入力カラープロファイル カラープロファイルを埋め込まないRGBマテリアル画像やビネット、およびbgc=やcolor=などの様々なImage Renderingコマンドで指定されたRGBカラー値に使用するICCカラープロファイルの名前を指定します。
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 1c90c77c-79b7-41aa-9269-b48d966ba362
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 2%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

RGBの初期設定の入力カラープロファイル カラープロファイルを埋め込まないRGBマテリアル画像やビネット、およびbgc=やcolor=などの様々なImage Renderingコマンドで指定されたRGBカラー値に使用するICCカラープロファイルの名前を指定します。

## プロパティ {#section-c22966bba03e43c08e9d3fb91bfdd465}

テキスト文字列。 指定する場合、この画像カタログまたはデフォルトカタログのICCプロファイルマップの有効な`icc::Name`値、または`attribute::RootPath`を基準とするファイルパスを指定する必要があります。 参照されるICCプロファイルは、RGBプロファイルである必要があります。

## 初期設定 {#section-0171cd6680284bfa9844b9cc3644ca61}

`default::IccProfileSrcRgb`から継承されます（定義されていない場合または空の場合）。 `attribute::IccProfileSrcRgb`が有効なプロファイルに解決されない場合は、代わりに`attribute::IccProfileRgb`が使用されます。

## 関連項目 {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) 、 [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)、 [attribute::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30)、 [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
