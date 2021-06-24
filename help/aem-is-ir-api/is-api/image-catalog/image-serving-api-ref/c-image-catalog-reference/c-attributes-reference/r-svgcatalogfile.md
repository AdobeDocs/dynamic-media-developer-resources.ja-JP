---
description: SVGデータファイルのパス。 このカタログのSVGデータを含むファイルを指定します。
solution: Experience Manager
title: SvgCatalogFile
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 654579a2-33ff-4633-a6d0-3c03ec8d5aed
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 4%

---

# SvgCatalogFile{#svgcatalogfile}

SVGデータファイルのパス。 このカタログのSVGデータを含むファイルを指定します。

SVGデータファイルは、すべての画像データファイルの後に、指定された順序で読み込まれます。 同じ`catalog::Id`値が複数のレコードに存在する場合（同じ画像または異なる画像またはSVGカタログファイル内）、最後のインスタンスが優先されます。

## プロパティ {#section-fc2d549f76474792837b2b92ec2087ea}

コンマ区切りの1つ以上のテキスト文字列値。 （オプション）各値は、絶対ファイルパスまたはカタログフォルダーを基準とした相対パスである必要があります。

## 初期設定 {#section-a4e58951f3c249599665b823566433c9}

空の場合、この画像カタログにSVGデータが含まれていないことを示します。

## 関連項目 {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[カタログデータ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)、カタ [ログファイル](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
