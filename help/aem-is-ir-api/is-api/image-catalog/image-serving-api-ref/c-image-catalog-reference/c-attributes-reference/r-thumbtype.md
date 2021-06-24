---
description: 初期設定のサムネールの種類。 特定のカタログレコードに有効なカタログThumbType値が含まれていない場合のサムネールタイプのデフォルトを指定します。
solution: Experience Manager
title: ThumbType
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: ac29ac3a-8c6b-4c87-954f-37d1ddec76f5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---

# ThumbType{#thumbtype}

初期設定のサムネールの種類。 特定のカタログレコードに有効なcatalog::ThumbType値が含まれていない場合のサムネールタイプのデフォルトを指定します。

サムネール要求(`req=tmb`)にのみ使用されます。

## プロパティ {#section-ae0babfe3c8e4c8ebe0124bc55051265}

列挙 指定できる値は、 *`crop`* 、 *`fit`* 、 *`texture`*&#x200B;の各サムネールタイプで、それぞれ1、2、3です。

## 初期設定 {#section-0237fcae4f304c5b876fceaa839b6b05}

`default::ThumbType`から継承されます（定義されていない場合または空の場合）。

## 関連項目 {#section-986c97470c494bfd8f179cecf8cc3ccc}

[catalog::ThumbType](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03)
