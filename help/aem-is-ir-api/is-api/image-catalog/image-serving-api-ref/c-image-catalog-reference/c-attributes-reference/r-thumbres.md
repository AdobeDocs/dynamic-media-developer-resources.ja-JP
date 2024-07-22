---
description: デフォルトのサムネール解像度。 特定のカタログレコードに有効なカタログ ThumbRes の値が含まれていない場合に使用する、サムネールオブジェクト解像度のデフォルトを指定します。
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0abb680e-8944-4ad8-9b6c-d0a7559fdd1b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---

# ThumbRes{#thumbres}

デフォルトのサムネール解像度。 特定のカタログレコードに有効な catalog::ThumbRes の値が含まれていない場合に使用する、サムネールオブジェクト解像度のデフォルトを指定します。

サムネールリクエスト（`req=tmb`）にのみ使用され、`catalog::ThumbType=3` の場合に使用されます。

## プロパティ {#section-88d37d0e030f4879a9e584dd2cc780f3}

0.より大きい実数。通常は 1 インチあたりのピクセル数で表されますが、1 メートルあたりのピクセル数など、他の単位の場合もあります。

## 初期設定 {#section-86588899ec9b4276a98b03d7faf64003}

定義されていない場合または空の場合は `default::ThumbRes` から継承します。

## 関連項目 {#section-a6d2cce2e404441a996dba98a95c8e16}

[カタログ：:ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
