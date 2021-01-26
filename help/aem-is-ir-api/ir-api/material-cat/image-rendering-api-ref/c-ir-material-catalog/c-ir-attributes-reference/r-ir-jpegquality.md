---
description: 初期設定のJPEGエンコーディング画質。 JPEGでエンコードされた返信画像の初期設定の画質設定を指定します。
seo-description: 初期設定のJPEGエンコーディング画質。 JPEGでエンコードされた返信画像の初期設定の画質設定を指定します。
seo-title: JpegQuality
solution: Experience Manager
title: JpegQuality
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 82dabdae-a1f3-484a-a520-ae765914d0f7
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 4%

---


# JpegQuality{#jpegquality}

初期設定のJPEGエンコーディング画質。 JPEGでエンコードされた返信画像の初期設定の画質設定を指定します。

## プロパティ {#section-8b1ed3e0acaa4fbfa050b74c00b9d4dc}

整数の数値とフラグ（カンマ区切り）。 最初の値は1 ～ 100の範囲で、クォリティを定義します。 2番目の値は、通常の動作では0に設定できます。また、JPEGエンコーダーで通常使用される色度ダウンサンプリングを無効にする場合は1に設定します。

## 初期設定 {#section-60900c0fb8c54444b2361513232514db}

定義されていない場合や空の場合は`default::JpegQuality`から継承されます。

## 関連項目 {#section-8928a28fcbfe401cad4d4021a7a1c268}

[qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)
