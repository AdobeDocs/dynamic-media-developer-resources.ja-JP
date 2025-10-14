---
description: SVG データファイルのパス。 このカタログのSVG データを含むファイルを指定します。
solution: Experience Manager
title: SvgCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 654579a2-33ff-4633-a6d0-3c03ec8d5aed
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 2%

---

# SvgCatalogFile{#svgcatalogfile}

SVG データファイルのパス。 このカタログのSVG データを含むファイルを指定します。

SVG データファイルは、すべての画像データファイルの後に、指定された順序で読み込まれます。 同じ `catalog::Id` 値が複数のレコード（同じ画像または異なる画像またはSVG カタログファイル）で発生した場合は、最後のインスタンスが優先されます。

## プロパティ {#section-fc2d549f76474792837b2b92ec2087ea}

コンマで区切られた 1 つ以上のテキスト文字列値。 オプション。 各値は、絶対ファイルパスまたはカタログフォルダーを基準とした相対パスである必要があります。

## 初期設定 {#section-a4e58951f3c249599665b823566433c9}

空（この画像カタログにSVG データが含まれていないことを示します）。

## 関連項目 {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[&#x200B; カタログ データ &#x200B;](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)、[&#x200B; カタログ ファイル &#x200B;](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
