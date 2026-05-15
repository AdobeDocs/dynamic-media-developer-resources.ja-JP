---
title: JpegQuality
description: JPEGのデフォルトのエンコーディング品質。 JPEGでエンコードされた返信画像のデフォルトの画質設定を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a699a9e-dbf6-4e01-95aa-37a6eb83f4df
TQID: 'https://experienceleague.adobe.com/h7SBTIJh-a1Z0e3hfMA5TSXDI3ft809TrWyCggl8loU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 3%

---

# JpegQuality{#jpegquality}

JPEGのデフォルトのエンコーディング品質。 JPEGでエンコードされた返信画像のデフォルトの画質設定を指定します。

## プロパティ {#section-8b1ed3e0acaa4fbfa050b74c00b9d4dc}

整数とフラグ。コンマで区切ります。 最初の値は1..100の範囲にあり、品質を定義します。 2番目の値は、通常のビヘイビアーの場合は`0`、JPEG エンコーダが使用する色度ダウンサンプリングを無効にする場合は`1`です。

## 初期設定 {#section-60900c0fb8c54444b2361513232514db}

定義されていない場合や空の場合は、`default::JpegQuality`から継承されます。

## 関連項目 {#section-8928a28fcbfe401cad4d4021a7a1c268}

[qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)
