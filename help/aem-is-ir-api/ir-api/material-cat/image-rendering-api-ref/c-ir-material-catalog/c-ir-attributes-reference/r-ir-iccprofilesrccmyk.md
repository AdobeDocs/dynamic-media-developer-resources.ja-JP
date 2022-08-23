---
title: IccProfileSrcCmyk
description: CMYK の初期設定入力カラープロファイル。 カラープロファイルを埋め込まない CMYK マテリアル画像に使用する ICC カラープロファイルの名前を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 09be34c8-facc-40c3-ba15-c48bd93b3be1
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK の初期設定入力カラープロファイル。 カラープロファイルを埋め込まない CMYK マテリアル画像に使用する ICC カラープロファイルの名前を指定します。

## プロパティ {#section-0cee77438d914c319ec876edb3490821}

テキスト文字列。 指定する場合、有効な `icc::Name` この画像カタログまたはデフォルトカタログの ICC プロファイルマップからの値、または `attribute::RootPath`. 参照される ICC プロファイルは CMYK プロファイルである必要があります。

## 初期設定 {#section-11f6239e0dd14827abf4a95c1b30161c}

継承元 `default::IccProfileSrcCmyk` が定義されていない場合、または空の場合は。 If `attribute::IccProfileSrcCmyk` は有効なプロファイルに解決されません。 `attribute::IccProfileCmyk` が代わりに使用されます。

## 関連項目 {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
