---
description: 解像度. 「現実世界」の画像解像度。通常は1インチあたりのピクセル数で表されますが、他の単位（1メートルあたりのピクセル数など）で表す場合もあります。
solution: Experience Manager
title: 解像度
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 45b12324-3148-4530-82cd-0ee32e9f98f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 7%

---

# 解像度{#resolution}

解像度. 「現実世界」の画像解像度。通常は1インチあたりのピクセル数で表されますが、他の単位（1メートルあたりのピクセル数など）で表す場合もあります。

## プロパティ {#section-985ca2ad858c4e9c9cbb303f55447553}

0より大きい実数。 イメージ解像度がattribute::Resolutionと同じでない限り、テクスチャマテリアルとデカールマテリアルに必要です。 ソリッドカラーとキャビネットのマテリアルでは無視されます。

## 初期設定 {#section-b1d044e211194242a900aaef4a8c8e6f}

`attribute::Resolution` は、フィールドが存在しない場合、値が0または負の場合、またはフィールドが空の場合に使用されます。

## 関連項目 {#section-2d04df523d7345f6929178cbc637da78}

[attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-09fe14e6bfbf4db6b7f4369fffecc806) ,  [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)
