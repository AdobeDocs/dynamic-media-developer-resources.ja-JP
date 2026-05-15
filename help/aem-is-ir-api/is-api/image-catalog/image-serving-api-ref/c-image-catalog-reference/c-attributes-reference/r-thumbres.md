---
description: デフォルトのサムネール解像度。 特定のカタログレコードに有効なカタログのThumbRes値が含まれていない場合のサムネールオブジェクト解決のデフォルトを提供します。
solution: Experience Manager
title: サムレス
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0abb680e-8944-4ad8-9b6c-d0a7559fdd1b
TQID: 'https://experienceleague.adobe.com/xMGMMjCIDWQJbJtLzatEiSEgdD5hQOkaOhKJbMYUyB0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 3%

---

# サムレス{#thumbres}

デフォルトのサムネール解像度。 特定のカタログレコードに有効なcatalog::ThumbRes値が含まれていない場合のサムネールオブジェクト解決のデフォルトを提供します。

サムネール要求（`req=tmb`）と`catalog::ThumbType=3`の場合にのみ使用されます。

## プロパティ {#section-88d37d0e030f4879a9e584dd2cc780f3}

実数（0）より大きい。通常は1 インチあたりのピクセルとして表されますが、メートルあたりのピクセルなど、他の単位でも表されます。

## 初期設定 {#section-86588899ec9b4276a98b03d7faf64003}

定義されていない場合や空の場合は、`default::ThumbRes`から継承されます。

## 関連項目 {#section-a6d2cce2e404441a996dba98a95c8e16}

[catalog::ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
