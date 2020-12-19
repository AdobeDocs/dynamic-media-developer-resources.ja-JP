---
description: 解像度. 「現実の」画像解像度。通常はピクセル/インチで表されますが、他の単位（ピクセル/メートルなど）でも使用できます。
seo-description: 解像度. 「現実の」画像解像度。通常はピクセル/インチで表されますが、他の単位（ピクセル/メートルなど）でも使用できます。
seo-title: 解像度
solution: Experience Manager
title: 解像度
topic: Scene7 Image Serving - Image Rendering API
uuid: 281c7ff6-8f78-4654-98ec-0db4299b80d9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 8%

---


# 解像度{#resolution}

解像度. 「現実の」画像解像度。通常はピクセル/インチで表されますが、他の単位（ピクセル/メートルなど）でも使用できます。

## プロパティ {#section-985ca2ad858c4e9c9cbb303f55447553}

0より大きい実数。 イメージの解像度がattribute::Resolutionと同じでない限り、テクスチャおよびデカールのマテリアルに必要です。 べた塗りとキャビネットのマテリアルでは無視されます。

## 初期設定 {#section-b1d044e211194242a900aaef4a8c8e6f}

`attribute::Resolution` は、フィールドが存在しない場合、値が0または負の場合、またはフィールドが空の場合に使用されます。

## 関連項目 {#section-2d04df523d7345f6929178cbc637da78}

[attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-09fe14e6bfbf4db6b7f4369fffecc806) ,  [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)
