---
description: 初期設定のJPEGエンコーディング属性 JPEG返信画像の初期設定の属性を指定します。
seo-description: 初期設定のJPEGエンコーディング属性 JPEG返信画像の初期設定の属性を指定します。
seo-title: JpegQuality
solution: Experience Manager
title: JpegQuality
topic: Scene7 Image Serving - Image Rendering API
uuid: c256c44c-2807-4a0c-b6e4-3de0a828feda
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---


# JpegQuality{#jpegquality}

初期設定のJPEGエンコーディング属性 JPEG返信画像の初期設定の属性を指定します。

## プロパティ {#section-7a75ebaf11bd4b778d287c2c5c150d0c}

整数の数値とフラグ（カンマ区切り）。 最初の値は1 ～ 100の範囲で、クォリティを定義します。 2番目の値は、通常の動作では0に、JPEGエンコーダーで通常使用されるRGB色度ダウンサンプリングを無効にする場合は1に設定します。

## 初期設定 {#section-0b25eddd59bc434abfe38eeea9d45df3}

定義されていない場合や空の場合は`default::JpegQuality`から継承されます。

## 関連項目 {#section-aa994afc02ea4f799655233ea32d36c9}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352)
