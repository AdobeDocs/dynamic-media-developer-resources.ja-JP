---
description: 相対画像URLのルートURL。 相対画像URLのルートURLを指定します。
solution: Experience Manager
title: RootUrl
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 72560180-53e5-4293-9dd3-c0cd196551dc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# RootUrl{#rooturl}

相対画像URLのルートURL。 相対画像URLのルートURLを指定します。

`attribute::RootUrl` またはの値が{中括弧}ま `attribute::RootPath` たは( `src=` 括 `mask=` 弧)で囲まれている場合は、代わりにが使用されます。

## プロパティ {#section-fe02269b4b724319a5d1f2cfcae31cba}

テキスト文字列の値。 先頭のプロトコル識別子を含む、絶対URLルートパス。 次のプロトコルがサポートされています。HTTP、HTTPS、FTP。

## 初期設定 {#section-fa5e3fc993c04086bc2b06dfeea4ae5c}

定義されていない場合は`default::RootUrl`から継承されます。 定義されているが空の場合、相対URLはこの画像カタログでサポートされません。

## 関連項目 {#section-ade4789086df4e76ae041cd4acfa2f85}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) 、 [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)、  [attribute:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)、  [ruleset::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)
