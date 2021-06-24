---
description: 初期設定のサムネール解像度。 特定のカタログレコードに有効なcatalog ThumbRes値が含まれていない場合の、サムネールオブジェクトの解像度のデフォルトを指定します。
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 0abb680e-8944-4ad8-9b6c-d0a7559fdd1b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---

# ThumbRes{#thumbres}

初期設定のサムネール解像度。 特定のカタログレコードに有効なcatalog::ThumbRes値が含まれていない場合の、サムネールオブジェクトの解像度のデフォルトを指定します。

サムネール要求(`req=tmb`)と`catalog::ThumbType=3`の場合にのみ使用されます。

## プロパティ {#section-88d37d0e030f4879a9e584dd2cc780f3}

0より大きい実数。通常は1インチあたりのピクセル数で表されますが、他の単位（1メートルあたりのピクセル数など）で表される場合もあります。

## 初期設定 {#section-86588899ec9b4276a98b03d7faf64003}

`default::ThumbRes`から継承されます（定義されていない場合または空の場合）。

## 関連項目 {#section-a6d2cce2e404441a996dba98a95c8e16}

[catalog::ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
