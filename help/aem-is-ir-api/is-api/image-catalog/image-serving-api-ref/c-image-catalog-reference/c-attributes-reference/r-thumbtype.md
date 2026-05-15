---
description: デフォルトのサムネールタイプ。 特定のカタログレコードに有効なカタログのThumbType値が含まれていない場合に備えて、サムネールタイプのデフォルトを指定します。
solution: Experience Manager
title: ThumbType
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac29ac3a-8c6b-4c87-954f-37d1ddec76f5
TQID: 'https://experienceleague.adobe.com/BoSwS4iXsvygzR69-5lupAwyynicSlYGRnITnpnSZuc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 82
ht-degree: 3%

---

# ThumbType{#thumbtype}

デフォルトのサムネールタイプ。 特定のカタログレコードに有効なcatalog::ThumbType値が含まれていない場合に備えて、サムネールタイプのデフォルトを指定します。

サムネール要求（`req=tmb`）にのみ使用されます。

## プロパティ {#section-ae0babfe3c8e4c8ebe0124bc55051265}

列挙： 使用できる値は、それぞれ&#x200B;*`crop`*、*`fit`*&#x200B;および&#x200B;*`texture`*&#x200B;のサムネール型に対して、1、2、および3です。

## 初期設定 {#section-0237fcae4f304c5b876fceaa839b6b05}

定義されていない場合や空の場合は、`default::ThumbType`から継承されます。

## 関連項目 {#section-986c97470c494bfd8f179cecf8cc3ccc}

[catalog::ThumbType](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03)
