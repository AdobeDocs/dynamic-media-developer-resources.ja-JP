---
description: 絶対 URL を画像ソースとして許可します。
solution: Experience Manager
title: AllowDirectUrls
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e160101a-9bb7-452f-b892-c2aa65e26e94
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 6%

---

# AllowDirectUrls{#allowdirecturls}

絶対 URL を画像ソースとして許可します。

`src=` および `mask=` コマンドに埋め込まれた絶対 URL のサポートを有効または無効にします。 無効にした場合、`attribute::RootUrl` に関連する URL のみが許可されます。

## プロパティ {#section-192825a6b02e4cc4a6aa102f93be89f0}

フラグ。

## 初期設定 {#section-c2eb9ab424db41c6aac91ba2cbe00ef5}

定義されていない場合または空の場合は `default::AllowDirectUrls` から継承します。

## 関連項目 {#section-604f9500749c4e1a968b260b9a3812b2}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute::RootUrl](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137)
