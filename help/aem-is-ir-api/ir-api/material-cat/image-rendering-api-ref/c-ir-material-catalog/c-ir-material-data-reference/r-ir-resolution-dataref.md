---
description: 解像度。 「実際の」画像解像度（通常は 1 インチあたりのピクセル数で表されますが、1 メートルあたりのピクセル数など、他の単位の場合もあります）。
solution: Experience Manager
title: 解像度
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 45b12324-3148-4530-82cd-0ee32e9f98f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---

# 解像度{#resolution}

解像度。 「実際の」画像解像度（通常は 1 インチあたりのピクセル数で表されますが、1 メートルあたりのピクセル数など、他の単位の場合もあります）。

## プロパティ {#section-985ca2ad858c4e9c9cbb303f55447553}

0 より大きい実数。 テクスチャ マテリアルとデカール マテリアルには必須です（イメージの解像度が attribute::Resolution と同じでない限り）。 単色およびキャビネット材料では無視されます。

## 初期設定 {#section-b1d044e211194242a900aaef4a8c8e6f}

`attribute::Resolution` は、フィールドが存在しない場合、値が 0 または負の場合、またはフィールドが空の場合に使用されます。

## 関連項目 {#section-2d04df523d7345f6929178cbc637da78}

[attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-09fe14e6bfbf4db6b7f4369fffecc806) , [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)
