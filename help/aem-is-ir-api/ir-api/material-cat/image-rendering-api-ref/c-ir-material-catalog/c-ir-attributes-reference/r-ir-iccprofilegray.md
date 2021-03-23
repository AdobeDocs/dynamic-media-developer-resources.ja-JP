---
description: グレースケールの初期設定カラースペース icc=で出力カラースペースが指定されていない場合に、グレースケールレスポンスプロファイルに使用するICCカラー画像の名前を指定します。
seo-description: グレースケールの初期設定カラースペース icc=で出力カラースペースが指定されていない場合に、グレースケールレスポンスプロファイルに使用するICCカラー画像の名前を指定します。
seo-title: IccProfileGray
solution: Experience Manager
title: IccProfileGray
uuid: 064be242-d964-4fb8-99ea-78bb5599e70f
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---


# IccProfileGray{#iccprofilegray}

グレースケールの初期設定カラースペース icc=で出力カラースペースが指定されていない場合に、グレースケールレスポンスプロファイルに使用するICCカラー画像の名前を指定します。

## プロパティ {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

テキスト文字列。 指定する場合、このマテリアルカタログまたは初期設定のカタログのICCプロファイルマップ、または`attribute::RootPath`を基準とするファイルパスの有効な`icc::Name`値である必要があります。 参照先のICCプロファイルは、グレースケールプロファイルである必要があります。

## 初期設定 {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

定義されていない場合や空の場合は`default::IccProfileGray`から継承されます。

## 関連項目 {#section-cd43189611f4426aacddcc604eb02a10}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileSrcGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
