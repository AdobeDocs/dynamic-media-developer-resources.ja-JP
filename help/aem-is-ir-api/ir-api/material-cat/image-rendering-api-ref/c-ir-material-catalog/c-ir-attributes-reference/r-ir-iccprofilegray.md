---
title: IccProfileGray
description: グレースケールのデフォルトカラースペース。 出力カラースペースが icc=で指定されていない場合に、グレースケール応答画像に使用する ICC カラープロファイルの名前を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 21f37090-a68c-4d86-a807-bda243a8f99e
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 2%

---

# IccProfileGray{#iccprofilegray}

グレースケールのデフォルトカラースペース。 `icc=` で出力カラースペースが指定されていない場合に、グレースケール応答画像に使用する ICC カラープロファイルの名前を指定します。

## プロパティ {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

テキスト文字列 指定する場合、このマテリアル カタログまたは既定のカタログの ICC プロファイル マップの有効な `icc::Name` 値、または `attribute::RootPath` に対する相対ファイル パスでなければなりません。 参照される ICC プロファイルは、グレースケールプロファイルである必要があります。

## 初期設定 {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

定義されていない場合または空の場合は `default::IccProfileGray` から継承します。

## 関連項目 {#section-cd43189611f4426aacddcc604eb02a10}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2)、[attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)、[attribute::IccProfileSrcGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2)、[attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
