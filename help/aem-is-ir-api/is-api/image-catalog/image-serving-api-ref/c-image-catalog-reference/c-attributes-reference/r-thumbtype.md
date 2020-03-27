---
description: 初期設定のサムネールの種類。 特定のカタログレコードに有効なカタログのThumbType値が含まれていない場合のサムネールの種類の初期設定を指定します。
seo-description: 初期設定のサムネールの種類。 特定のカタログレコードに有効なカタログのThumbType値が含まれていない場合のサムネールの種類の初期設定を指定します。
seo-title: ThumbType
solution: Experience Manager
title: ThumbType
topic: Scene7 Image Serving - Image Rendering API
uuid: 0b4aa767-2d80-4df8-8189-9d095cb88e87
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ThumbType{#thumbtype}

初期設定のサムネールの種類。 特定のカタログレコードに有効なcatalog::ThumbType値が含まれていない場合のサムネールの種類の初期設定を指定します。

サムネールリクエスト( `req=tmb`)にのみ使用されます。

## プロパティ {#section-ae0babfe3c8e4c8ebe0124bc55051265}

列挙。 使用できる値は、それぞれサムネールタイプに対して1、2 *`crop`*&#x200B;および3 *`fit`*&#x200B;で、サ *`texture`* ムネールタイプに対して3です。

## 初期設定 {#section-0237fcae4f304c5b876fceaa839b6b05}

定義されていな `default::ThumbType`い場合や空の場合に継承されます。

## 関連項目 {#section-986c97470c494bfd8f179cecf8cc3ccc}

[catalog::ThumbType](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03)
