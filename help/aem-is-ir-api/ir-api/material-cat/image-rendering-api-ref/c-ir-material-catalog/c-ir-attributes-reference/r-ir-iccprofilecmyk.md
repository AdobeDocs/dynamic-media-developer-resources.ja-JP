---
description: CMYKの初期設定のカラースペース。 icc=で出力カラースペースが指定されていない場合にグレースケールの応答画像に使用するICCカラープロファイルの名前を指定します。
seo-description: CMYKの初期設定のカラースペース。 icc=で出力カラースペースが指定されていない場合にグレースケールの応答画像に使用するICCカラープロファイルの名前を指定します。
seo-title: IccProfileCmyk
solution: Experience Manager
title: IccProfileCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: d923d0fd-f00b-4fce-8ce9-8b177b4dba96
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileCmyk{#iccprofilecmyk}

CMYKの初期設定のカラースペース。 icc=で出力カラースペースが指定されていない場合にグレースケールの応答画像に使用するICCカラープロファイルの名前を指定します。

## プロパティ {#section-849678b272954bdcb236f49aa54f1609}

テキスト文字列。 指定する場合、この画像カタログま `icc::Name` たは初期設定のカタログのICCプロファイルマップ、またはを基準とする相対ファイルパスの有効な値である必要がありま `attribute::RootPath`す。 参照先のICCプロファイルはCMYKプロファイルである必要があります。

## 初期設定 {#section-55026b7454af4d868bcb47f7743c9c5b}

定義されていな `default::IccProfileCmyk` い場合や空の場合に継承されます。

## 関連項目 {#section-89feb193693b43dc99a2107658d57154}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) 、 [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)、 [attribute::IccProfileSrcCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrccmyk.md#reference-0256cae955404ebc92d5d0d1fa095ea2)、 [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
