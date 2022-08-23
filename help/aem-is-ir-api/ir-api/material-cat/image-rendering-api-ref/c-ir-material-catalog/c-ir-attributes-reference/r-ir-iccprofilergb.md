---
title: IccProfileRgb
description: RGBのデフォルトの出力カラープロファイル。 icc=で出力カラースペースが指定されていない場合に、RGB応答画像に使用する ICC カラープロファイルの名前を指定します。 また、bgc=や color=など、様々なRGBレンダリングコマンドで指定された特定の画像カラー値の場合も同様です。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4057e968-24de-41af-9901-a6cb5ed9ea63
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# IccProfileRgb{#iccprofilergb}

RGBのデフォルトの出力カラープロファイル。 で出力カラースペースが指定されていない場合に、RGB応答画像に使用する ICC カラープロファイルの名前を指定します。 `icc=`. また、各種のRGBレンダリングコマンドで指定された特定の画像カラー値 ( `bgc=` および `color=`.

## プロパティ {#section-b4a1bd92e99047479a5036413525a6d9}

テキスト文字列。 指定する場合、有効な `icc::Name` このマテリアルカタログまたはデフォルトカタログの ICC プロファイルマップ、または `attribute::RootPath`. 参照される ICC プロファイルは、RGBプロファイルである必要があります。

## 初期設定 {#section-5809772f8e96438ab7626d323c66a4ba}

継承元 `default::IccProfileRgb` が定義されていない場合、または空の場合は。

## 関連項目 {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
