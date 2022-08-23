---
title: IccProfileSrcRgb
description: RGBの初期設定の入力カラープロファイル。 カラープロファイルを埋め込まないRGB素材画像やビネットに使用する ICC カラープロファイルの名前を指定します。 また、bgc=や color=など、様々なRGBレンダリングコマンドで指定された画像カラー値の場合も使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c90c77c-79b7-41aa-9269-b48d966ba362
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 2%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

RGBの初期設定の入力カラープロファイル。 カラープロファイルを埋め込まないRGB素材画像やビネットに使用する ICC カラープロファイルの名前を指定します。 また、RGBのカラー値の場合、 `bgc=` および `color=`.

## プロパティ {#section-c22966bba03e43c08e9d3fb91bfdd465}

テキスト文字列。 指定する場合、有効な `icc::Name` この画像カタログまたはデフォルトカタログの ICC プロファイルマップからの値、または `attribute::RootPath`. 参照される ICC プロファイルは、RGBプロファイルである必要があります。

## 初期設定 {#section-0171cd6680284bfa9844b9cc3644ca61}

継承元 `default::IccProfileSrcRgb` が定義されていない場合、または空の場合は。 If `attribute::IccProfileSrcRgb` は有効なプロファイルに解決されません。 `attribute::IccProfileRgb` が代わりに使用されます。

## 関連項目 {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
