---
description: CMYKのデフォルト出力カラープロファイル。 icc=で出力カラースペースが指定されていない場合にCMYK応答画像に使用するICC カラープロファイルの名前を指定します。また、color=など、様々な画像サービングコマンドで指定された特定のCMYK カラー値に対して使用します。
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2bf83cf5-3fc9-42aa-a143-4b56e43ee4d1
TQID: 'https://experienceleague.adobe.com/G0UbfC77naL9ki0QEcpEYCX5Z4Tr3wt7YL2bQi8ZNEI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 148
ht-degree: 2%

---

# IccProfileCmyk{#iccprofilecmyk}

CMYKのデフォルト出力カラープロファイル。 icc=で出力カラースペースが指定されていない場合にCMYK応答画像に使用するICC カラープロファイルの名前を指定します。また、color=など、様々な画像サービングコマンドで指定された特定のCMYK カラー値に対して使用します。

## プロパティ {#section-d8b6102cc1c744d482f99808ccfcaa24}

テキスト文字列。 指定する場合は、この画像カタログまたはデフォルトカタログのICC プロファイルマップからの有効な`icc::Name`値、または`attribute::RootPath`に対するファイルパスである必要があります。 参照されるICC プロファイルは、CMYK プロファイルである必要があります。

## 初期設定 {#section-62442df09a724950bfbdd0640b3e6678}

定義されていない場合や空の場合は、`default::IccProfileCmyk`から継承されます。

## 関連項目 {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe)、[属性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)、[属性：:IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)、[属性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
