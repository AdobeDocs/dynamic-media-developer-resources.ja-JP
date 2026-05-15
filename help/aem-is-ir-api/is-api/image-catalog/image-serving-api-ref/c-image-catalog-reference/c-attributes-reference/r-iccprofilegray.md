---
title: IccProfileGray
description: グレースケールのデフォルト出力カラープロファイル。 icc=で出力カラースペースが指定されていない場合にグレースケール応答画像に使用するICC カラープロファイルの名前を指定します。また、color=など、様々な画像サービングコマンドで指定された特定のグレースケールカラー値に対して使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4964c3b3-799d-40cb-bc5f-d08acfd41ed9
TQID: 'https://experienceleague.adobe.com/brb4FvAJ9aMt3FylkuDbuRMEGabGuRqWBVD2Yu1y4os'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 148
ht-degree: 2%

---

# IccProfileGray{#iccprofilegray}

グレースケールのデフォルト出力カラープロファイル。 icc=で出力カラースペースが指定されていない場合にグレースケール応答画像に使用するICC カラープロファイルの名前を指定します。また、color=など、様々な画像サービングコマンドで指定された特定のグレースケールカラー値に対して使用します。

## プロパティ {#section-03f090ee2acf4537b83f78840d23ecab}

テキスト文字列。 指定する場合は、この画像カタログまたはデフォルトカタログのICC プロファイルマップからの有効な`icc::Name`値、または`attribute::RootPath`に対するファイルパスである必要があります。 参照されるICC プロファイルは、グレースケールプロファイルである必要があります。

## 初期設定 {#section-95ba3ab15edc4259b657c6ebf8783d61}

定義されていない場合や空の場合は、`default::IccProfileGray`から継承されます。

## 関連項目 {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe)、[属性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)、[属性：:IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)、[属性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
