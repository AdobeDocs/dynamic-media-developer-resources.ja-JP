---
description: 相対画像URLのルートURL 相対画像URLのルートURLを指定します。
seo-description: 相対画像URLのルートURL 相対画像URLのルートURLを指定します。
seo-title: RootUrl
solution: Experience Manager
title: RootUrl
topic: Scene7 Image Serving - Image Rendering API
uuid: 173ce99a-f87e-4700-a28a-1a87b8c55b85
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---


# RootUrl{#rooturl}

相対画像URLのルートURL 相対画像URLのルートURLを指定します。

`attribute::RootUrl` は、 `attribute::RootPath` または `src=`  `mask=` 値が{波括弧}または（丸括弧）で囲まれている場合の代わりに使用されます。

## プロパティ {#section-fe02269b4b724319a5d1f2cfcae31cba}

テキスト文字列の値。 先頭のプロトコル識別子を含む、絶対URLルートパス。 次のプロトコルがサポートされています。HTTP、HTTPSおよびFTP。

## 初期設定 {#section-fa5e3fc993c04086bc2b06dfeea4ae5c}

定義されていない場合は`default::RootUrl`から継承されます。 定義済みで空の場合、相対URLはこの画像カタログではサポートされません。

## 関連項目 {#section-ade4789086df4e76ae041cd4acfa2f85}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [attribute:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [ruleset::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)
