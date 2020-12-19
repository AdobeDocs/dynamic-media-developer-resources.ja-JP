---
description: SVGデータファイルのパス このカタログのSVGデータを含むファイルを指定します。
seo-description: SVGデータファイルのパス このカタログのSVGデータを含むファイルを指定します。
seo-title: SvgCatalogFile
solution: Experience Manager
title: SvgCatalogFile
topic: Scene7 Image Serving - Image Rendering API
uuid: f0c8e687-77cc-4ca7-b2c2-6ba8960e11e6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

---


# SvgCatalogFile{#svgcatalogfile}

SVGデータファイルのパス このカタログのSVGデータを含むファイルを指定します。

SVGデータファイルは、すべての画像データファイルの後に、指定した順序で読み込まれます。 同じ`catalog::Id`値が複数のレコード（同じレコード、別の画像、SVGカタログファイルのいずれか）に存在する場合は、最後のインスタンスが使用されます。

## プロパティ {#section-fc2d549f76474792837b2b92ec2087ea}

カンマで区切られた1つ以上のテキスト文字列値。 （オプション）各値は、絶対ファイルパスまたはカタログフォルダーを基準とした相対パスで指定する必要があります。

## 初期設定 {#section-a4e58951f3c249599665b823566433c9}

空（この画像カタログにはSVGデータが含まれていません）。

## 関連項目 {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[カタログデータ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)、 [CatalogFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
