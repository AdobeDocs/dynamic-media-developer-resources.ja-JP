---
description: カラー変換ディザリング。 icc=で明示的な選択が行われない場合に、カラー変換の知覚的な品質を向上させるためにディザリングを使用する必要があるかどうかを指定します。
solution: Experience Manager
title: IccDither
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4b444f0f-2313-4477-8a22-7840b4783c88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 3%

---

# IccDither{#iccdither}

カラー変換ディザリング。 icc=で明示的な選択が行われない場合に、カラー変換の知覚的な品質を向上させるためにディザリングを使用する必要があるかどうかを指定します。

## プロパティ {#section-b7ba44d2d5de43f5a0841fe4cac29d35}

フラグ。 0 に設定すると無効になり、1 に設定するとディザリングが有効になります。

## 初期設定 {#section-86c4230a16454464880f64d4ab5ad533}

定義されていない場合または空の場合は `default::IccDither` から継承します。

## 関連項目 {#section-fe119006eb414a618b6ec9edbed8fe94}

[attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md) &#42;, [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
