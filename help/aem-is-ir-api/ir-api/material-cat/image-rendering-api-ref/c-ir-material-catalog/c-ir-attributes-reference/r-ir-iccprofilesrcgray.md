---
title: IccProfileSrcGray
description: グレースケールのデフォルト入力カラープロファイル。 カラープロファイルを埋め込まないグレースケール マテリアル画像に使用するICC カラープロファイルの名前を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8c89f0bb-4912-4838-a9e2-fb5d2f255eae
TQID: 'https://experienceleague.adobe.com/j5-F9hrRAYN08NS62Pua7eda-5mlpOOMrdTLIj7Ww6g'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 2%

---

# IccProfileSrcGray{#iccprofilesrcgray}

グレースケールのデフォルト入力カラープロファイル。 カラープロファイルを埋め込まないグレースケール マテリアル画像に使用するICC カラープロファイルの名前を指定します。

## プロパティ {#section-97923d8561b845309442d57d017d91a4}

テキスト文字列。 指定する場合は、この画像カタログまたはデフォルトカタログのICC プロファイルマップからの有効な`icc::Name`値、または`attribute::RootPath`に対するファイルパスである必要があります。 参照されるICC プロファイルは、グレースケールプロファイルである必要があります。

## 初期設定 {#section-02c52805ee13483dba7878aeab51f889}

定義されていない場合や空の場合は、`default::IccProfileSrcGray`から継承されます。 `attribute::IccProfileSrcGray`が有効なプロファイルに解決しない場合は、代わりに`attribute::IccProfileGray`が使用されます。

## 関連項目 {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2)、[属性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)、[属性：:IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6)、[属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)

