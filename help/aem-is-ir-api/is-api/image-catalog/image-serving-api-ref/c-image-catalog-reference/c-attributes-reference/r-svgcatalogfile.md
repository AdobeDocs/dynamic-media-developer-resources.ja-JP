---
description: SVG データファイルのパス。 このカタログのSVG データを含むファイルを指定します。
solution: Experience Manager
title: SvgCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 654579a2-33ff-4633-a6d0-3c03ec8d5aed
TQID: 'https://experienceleague.adobe.com/m1-nKj-KiVQlN70GYy1AFAAQN-M1wnxTGmmj-e3t9AY'
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
ht-degree: 3%

---

# SvgCatalogFile{#svgcatalogfile}

SVG データファイルのパス。 このカタログのSVG データを含むファイルを指定します。

SVG データファイルは、指定した正確な順序で、すべての画像データファイルの後に読み込まれます。 同じ`catalog::Id`値が複数のレコード（同じ画像または異なる画像またはSVG カタログファイル）で発生する場合は、最後のインスタンスが優先されます。

## プロパティ {#section-fc2d549f76474792837b2b92ec2087ea}

1つ以上のテキスト文字列値をコンマで区切ります。 オプション。 各値は、カタログフォルダーに関連する絶対ファイルパスまたはパスである必要があります。

## 初期設定 {#section-a4e58951f3c249599665b823566433c9}

空。この画像カタログにSVG データが含まれていないことを示します。

## 関連項目 {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[&#x200B; カタログデータ &#x200B;](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)、[&#x200B; カタログファイル &#x200B;](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
