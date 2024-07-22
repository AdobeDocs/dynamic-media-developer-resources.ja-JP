---
description: デフォルトのサムネールの種類。 特定のカタログレコードに有効なカタログの ThumbType の値が含まれていない場合に使用する、デフォルトのサムネールの種類を指定します。
solution: Experience Manager
title: ThubType
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac29ac3a-8c6b-4c87-954f-37d1ddec76f5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 3%

---

# ThubType{#thumbtype}

デフォルトのサムネールの種類。 特定のカタログレコードに有効な catalog::ThumbType の値が含まれていない場合に使用する、デフォルトのサムネールの種類を指定します。

サムネールリクエスト（`req=tmb`）にのみ使用されます。

## プロパティ {#section-ae0babfe3c8e4c8ebe0124bc55051265}

列挙値。 使用できる値は、*`crop`*、*`fit`*、*`texture`* のサムネールのタイプに対して、それぞれ 1、2、3 です。

## 初期設定 {#section-0237fcae4f304c5b876fceaa839b6b05}

定義されていない場合 `default::ThumbType` または空の場合に、から継承。

## 関連項目 {#section-986c97470c494bfd8f179cecf8cc3ccc}

[カタログ：:ThumbType](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03)
