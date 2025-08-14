---
title: IccProfileSrcRgb
description: RGBのデフォルト入力カラープロファイル。 カラープロファイルを埋め込まないRGBのマテリアル画像およびビネットに使用する ICC カラープロファイルの名前を指定します。 また、様々な画像レンダリングコマンド（bgc=や color=など）で指定されたRGB カラー値の場合も同様です。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c90c77c-79b7-41aa-9269-b48d966ba362
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

RGBのデフォルト入力カラープロファイル。 カラープロファイルを埋め込まないRGBのマテリアル画像およびビネットに使用する ICC カラープロファイルの名前を指定します。 また、様々な画像レンダリングコマンド（`bgc=` や `color=` など）で指定したRGBのカラー値の場合も同様です。

## プロパティ {#section-c22966bba03e43c08e9d3fb91bfdd465}

テキスト文字列 指定する場合、は、この画像カタログまたはデフォルトのカタログの ICC プロファイルマップの有効な `icc::Name` 値、または `attribute::RootPath` に対する相対ファイルパスである必要があります。 参照される ICC プロファイルは、RGB プロファイルである必要があります。

## 初期設定 {#section-0171cd6680284bfa9844b9cc3644ca61}

定義されていない場合または空の場合は `default::IccProfileSrcRgb` から継承します。 `attribute::IccProfileSrcRgb` が有効なプロファイルに解決されない場合は、代わりに `attribute::IccProfileRgb` が使用されます。

## 関連項目 {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2)、[attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)、[attribute::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30)、[attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
