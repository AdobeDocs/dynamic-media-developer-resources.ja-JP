---
description: デフォルトのJPEG エンコーディング属性。 JPEG返信画像のデフォルト属性を指定します。
solution: Experience Manager
title: JpegQuality
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a7f7f9-0c2c-4421-9dbc-d5c1e936f0f1
TQID: 'https://experienceleague.adobe.com/eiTYLhEUblxZFnJJf5cWgrHF4qglIYB72m-COXeGc5A'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 3%

---

# JpegQuality{#jpegquality}

デフォルトのJPEG エンコーディング属性。 JPEG返信画像のデフォルト属性を指定します。

## プロパティ {#section-7a75ebaf11bd4b778d287c2c5c150d0c}

整数とフラグ。コンマで区切ります。 最初の値は1..100の範囲にあり、品質を定義します。 2番目の値は、通常のビヘイビアーに対しては0で、通常はJPEG エンコーダが使用するRGB色度のダウンサンプリングを無効にする場合は1です。

## 初期設定 {#section-0b25eddd59bc434abfe38eeea9d45df3}

定義されていない場合や空の場合は、`default::JpegQuality`から継承されます。

## 関連項目 {#section-aa994afc02ea4f799655233ea32d36c9}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352)
