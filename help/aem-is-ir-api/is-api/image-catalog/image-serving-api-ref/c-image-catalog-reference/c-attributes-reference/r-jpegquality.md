---
description: デフォルトのJPEGエンコーディング属性。 JPEG返信画像のデフォルトの属性を指定します。
solution: Experience Manager
title: JpegQuality
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a7f7f9-0c2c-4421-9dbc-d5c1e936f0f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 3%

---

# JpegQuality{#jpegquality}

デフォルトのJPEGエンコーディング属性。 JPEG返信画像のデフォルトの属性を指定します。

## プロパティ {#section-7a75ebaf11bd4b778d287c2c5c150d0c}

整数とフラグ（コンマ区切り）。 最初の値は 1 ～ 100 の範囲で、画質を定義します。 2 つ目の値は、通常動作の場合は 0 を指定し、JPEGエンコーダで通常使用されるRGB色度ダウンサンプリングを無効にするには 1 を指定します。

## 初期設定 {#section-0b25eddd59bc434abfe38eeea9d45df3}

定義されていない場合または空の場合は `default::JpegQuality` から継承します。

## 関連項目 {#section-aa994afc02ea4f799655233ea32d36c9}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352)
