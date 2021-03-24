---
description: RGB初期設定の入力カラープロファイル カラー画像を埋め込まないRGBマテリアルプロファイルやビネット、およびbgc=やcolor=などの各種のImage Renderingコマンドで指定されたRGBカラー値に使用するICCカラープロファイルの名前を指定します。
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB初期設定の入力カラープロファイル カラー画像を埋め込まないRGBマテリアルプロファイルやビネット、およびbgc=やcolor=などの各種のImage Renderingコマンドで指定されたRGBカラー値に使用するICCカラープロファイルの名前を指定します。

## プロパティ {#section-c22966bba03e43c08e9d3fb91bfdd465}

テキスト文字列。 指定する場合、この画像カタログまたは初期設定のカタログのICCプロファイルマップの有効な`icc::Name`値、または`attribute::RootPath`を基準とするファイルパスである必要があります。 参照先のICCプロファイルはRGBプロファイルである必要があります。

## 初期設定 {#section-0171cd6680284bfa9844b9cc3644ca61}

定義されていない場合や空の場合は`default::IccProfileSrcRgb`から継承されます。 `attribute::IccProfileSrcRgb`が有効なプロファイルに解決されない場合は、代わりに`attribute::IccProfileRgb`が使用されます。

## 関連項目 {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
