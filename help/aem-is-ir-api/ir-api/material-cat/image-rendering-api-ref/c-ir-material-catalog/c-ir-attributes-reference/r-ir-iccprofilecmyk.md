---
description: CMYKの初期設定カラースペース icc=で出力カラースペースが指定されていない場合に、グレースケールの応答画像に使用するICCカラープロファイルの名前を指定します。
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: c36ea45d-dc91-4afa-825a-7af49738101c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# IccProfileCmyk{#iccprofilecmyk}

CMYKの初期設定カラースペース icc=で出力カラースペースが指定されていない場合に、グレースケールの応答画像に使用するICCカラープロファイルの名前を指定します。

## プロパティ {#section-849678b272954bdcb236f49aa54f1609}

テキスト文字列。 指定する場合、この画像カタログまたはデフォルトカタログのICCプロファイルマップの有効な`icc::Name`値、または`attribute::RootPath`を基準とするファイルパスを指定する必要があります。 参照されるICCプロファイルは、CMYKプロファイルである必要があります。

## 初期設定 {#section-55026b7454af4d868bcb47f7743c9c5b}

`default::IccProfileCmyk`から継承されます（定義されていない場合または空の場合）。

## 関連項目 {#section-89feb193693b43dc99a2107658d57154}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) 、 [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)、 [attribute::IccProfileSrcCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrccmyk.md#reference-0256cae955404ebc92d5d0d1fa095ea2)、 [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
