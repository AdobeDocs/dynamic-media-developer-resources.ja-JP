---
description: RGBのデフォルト出力カラープロファイル。 icc=で出力カラースペースが指定されていない場合や、color=などの様々なImage Serving コマンドで指定された特定のRGB カラー値に対して、RGB レスポンス画像に使用するICC カラープロファイルの名前を指定します。
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 861c7b54-6d18-47c8-a08d-970f29b63962
TQID: 'https://experienceleague.adobe.com/U9-XwSInZJDmRhDLPVzLqJds28LVZm3LkJE0iD7KEps'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 148
ht-degree: 2%

---

# IccProfileRgb{#iccprofilergb}

RGBのデフォルト出力カラープロファイル。 icc=で出力カラースペースが指定されていない場合や、color=などの様々なImage Serving コマンドで指定された特定のRGB カラー値に対して、RGB レスポンス画像に使用するICC カラープロファイルの名前を指定します。

## プロパティ {#section-3dd55c954d4d4ad4bb715ed7cee31025}

テキスト文字列。 指定する場合は、この画像カタログまたはデフォルトカタログのICC プロファイルマップからの有効な`icc::Name`値、または`attribute::RootPath`に対するファイルパスである必要があります。 参照されるICC プロファイルは、RGB プロファイルである必要があります。

## 初期設定 {#section-dfe08dd7b851453ca816623a4179955b}

定義されていない場合や空の場合は、`default::IccProfileRgb`から継承されます。

## 関連項目 {#section-05bc25ab7caa418ca94d43ced905add7}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe)、[属性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)、[属性：:IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)、[属性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
