---
title: IccProfileCmyk
description: CMYKのデフォルトのカラースペース。 icc=で出力カラースペースが指定されていない場合に、グレースケールの応答画像に使用するICC カラープロファイルの名前を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c36ea45d-dc91-4afa-825a-7af49738101c
TQID: 'https://experienceleague.adobe.com/EjbyUNxki4CNWJFUr-9QI8ygzLldCWO54HxN-7SE8dM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 2%

---

# IccProfileCmyk{#iccprofilecmyk}

CMYKのデフォルトのカラースペース。 出力カラースペースが`icc=`で指定されていない場合に、グレースケールの応答画像に使用するICC カラープロファイルの名前を指定します。

## プロパティ {#section-849678b272954bdcb236f49aa54f1609}

テキスト文字列。 指定する場合は、この画像カタログまたはデフォルトカタログのICC プロファイルマップからの有効な`icc::Name`値、または`attribute::RootPath`に対するファイルパスである必要があります。 参照されるICC プロファイルは、CMYK プロファイルである必要があります。

## 初期設定 {#section-55026b7454af4d868bcb47f7743c9c5b}

定義されていない場合や空の場合は、`default::IccProfileCmyk`から継承されます。

## 関連項目 {#section-89feb193693b43dc99a2107658d57154}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2)、[属性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)、[属性：:IccProfileSrcCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrccmyk.md#reference-0256cae955404ebc92d5d0d1fa095ea2)、[属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)

