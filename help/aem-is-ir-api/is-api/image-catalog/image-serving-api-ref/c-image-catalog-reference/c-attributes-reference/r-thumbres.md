---
description: 初期設定のサムネール解像度 特定のカタログレコードに有効なカタログThumbRes値が含まれていない場合に、サムネールオブジェクトの解像度の初期設定を指定します。
seo-description: 初期設定のサムネール解像度 特定のカタログレコードに有効なカタログThumbRes値が含まれていない場合に、サムネールオブジェクトの解像度の初期設定を指定します。
seo-title: ThumbRes
solution: Experience Manager
title: ThumbRes
topic: Scene7 Image Serving - Image Rendering API
uuid: 4a77d673-9d2e-4e62-a014-c99fa3df294a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---


# ThumbRes{#thumbres}

初期設定のサムネール解像度 特定のカタログレコードに有効なcatalog::ThumbRes値が含まれていない場合に、サムネールオブジェクトの解像度の初期設定を指定します。

サムネール要求(`req=tmb`)および`catalog::ThumbType=3`の場合にのみ使用されます。

## プロパティ {#section-88d37d0e030f4879a9e584dd2cc780f3}

0より大きい実数です。通常はピクセル/インチで表しますが、他の単位（ピクセル/メートルなど）で表すこともできます。

## 初期設定 {#section-86588899ec9b4276a98b03d7faf64003}

定義されていない場合や空の場合は`default::ThumbRes`から継承されます。

## 関連項目 {#section-a6d2cce2e404441a996dba98a95c8e16}

[catalog::ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
