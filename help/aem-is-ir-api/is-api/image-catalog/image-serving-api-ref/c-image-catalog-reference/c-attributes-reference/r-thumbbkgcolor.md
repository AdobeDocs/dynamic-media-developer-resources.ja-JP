---
description: サムネイルのデフォルトの背景色 出力サムネール画像内で実際の画像データが含まれない領域を埋めるために使用されるRGB値。
solution: Experience Manager
title: ThumbBkgColor
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88acf5ad-2973-42f9-9aaa-901e66b07f53
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# ThumbBkgColor{#thumbbkgcolor}

サムネイルのデフォルトの背景色 出力サムネール画像内で実際の画像データが含まれない領域を埋めるために使用されるRGB値。

サムネールリクエスト（`req=tmb`）にのみ使用され、`catalog::ThumbType` が 2 または 3 に設定されている場合に使用されます。

## プロパティ {#section-a73e82c950cc4319bc3bccec14764c25}

カラー。

## 初期設定 {#section-b02bb56dda684ff9969806ce82ba00c2}

定義されていない場合または空の場合は `default::ThumbBkgColor` から継承します。

## 関連項目 {#section-27983dc885424dfbba8c8e4192f3f88d}

[catalog::ThumbType](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03)、[req=tmb](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
