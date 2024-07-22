---
title: JpegQuality
description: デフォルトのJPEGエンコーディング品質。 JPEGエンコードされた返信画像の既定の品質設定を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a699a9e-dbf6-4e01-95aa-37a6eb83f4df
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# JpegQuality{#jpegquality}

デフォルトのJPEGエンコーディング品質。 JPEGエンコードされた返信画像の既定の品質設定を指定します。

## プロパティ {#section-8b1ed3e0acaa4fbfa050b74c00b9d4dc}

整数とフラグ（コンマ区切り）。 最初の値は 1 ～ 100 の範囲で、画質を定義します。 2 つ目の値は、通常の動作の場合は `0`、JPEGエンコーダで使用される色度ダウンサンプリングを無効にする場合は `1` です。

## 初期設定 {#section-60900c0fb8c54444b2361513232514db}

定義されていない場合または空の場合は `default::JpegQuality` から継承します。

## 関連項目 {#section-8928a28fcbfe401cad4d4021a7a1c268}

[qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)
