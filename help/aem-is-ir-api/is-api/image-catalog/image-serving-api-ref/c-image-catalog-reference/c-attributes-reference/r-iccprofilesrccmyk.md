---
title: IccProfileSrcCmyk
description: CMYK デフォルトの入力カラープロファイル。 カラープロファイルを埋め込まないCMYK ソース画像に使用するICC カラープロファイルの名前と、color=などの様々な画像サービングコマンドで指定された特定のCMYK カラー値を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 018170f3-2d1a-4da1-a480-b0a7e19457d8
TQID: 'https://experienceleague.adobe.com/ZzJlJzNfiGnMaKHqMpoJmOiEobxRcHeNAw-B78S3o78'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 155
ht-degree: 1%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK デフォルトの入力カラープロファイル。 カラープロファイルを埋め込まないCMYK ソース画像に使用するICC カラープロファイルの名前と、color=などの様々な画像サービングコマンドで指定された特定のCMYK カラー値を指定します。

## プロパティ {#section-fc2ad12a3c6e4c7cab495f1878638e66}

テキスト文字列。 指定する場合は、この画像カタログまたはデフォルトカタログのICC プロファイルマップからの有効な`icc::Name`値、または`attribute::RootPath`に対するファイルパスである必要があります。 参照されるICC プロファイルは、CMYK プロファイルである必要があります。

## 初期設定 {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

定義されていない場合や空の場合は、`default::IccProfileSrcCmyk`から継承されます。 `attribute::IccProfileSrcCmyk`が有効なプロファイルに解決しない場合は、代わりに`attribute::IccProfileCmyk`が使用されます。

## 関連項目 {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe)、[属性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)、[属性：:IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)、[属性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
