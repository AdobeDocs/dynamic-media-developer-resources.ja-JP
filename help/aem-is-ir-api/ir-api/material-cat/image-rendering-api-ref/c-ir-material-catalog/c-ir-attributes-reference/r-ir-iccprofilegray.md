---
title: IccProfileGray
description: グレースケールのデフォルトのカラースペース。 icc=で出力カラースペースが指定されていない場合に、グレースケール応答画像に使用するICC カラープロファイルの名前を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 21f37090-a68c-4d86-a807-bda243a8f99e
TQID: 'https://experienceleague.adobe.com/ZZOkc6f5V3-Luuwr5ku38nIy8snq4kh2lR4dqunXvFc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 115
ht-degree: 2%

---

# IccProfileGray{#iccprofilegray}

グレースケールのデフォルトのカラースペース。 出力カラースペースが`icc=`で指定されていない場合に、グレースケール応答画像に使用するICC カラープロファイルの名前を指定します。

## プロパティ {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

テキスト文字列。 指定する場合は、このマテリアル カタログまたは既定のカタログのICC プロファイル マップから有効な`icc::Name`値、または`attribute::RootPath`に関連するファイル パスである必要があります。 参照されるICC プロファイルは、グレースケールプロファイルである必要があります。

## 初期設定 {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

定義されていない場合や空の場合は、`default::IccProfileGray`から継承されます。

## 関連項目 {#section-cd43189611f4426aacddcc604eb02a10}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2)、[属性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)、[属性：:IccProfileSrcGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2)、[属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
