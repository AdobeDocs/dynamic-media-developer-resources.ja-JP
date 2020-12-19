---
description: 初期設定の解像度。 特定のカタログレコードに有効なカタログ解像度の値が含まれていない場合にデフォルトの解像度を指定します。
seo-description: 初期設定の解像度。 特定のカタログレコードに有効なカタログ解像度の値が含まれていない場合にデフォルトの解像度を指定します。
seo-title: 解像度
solution: Experience Manager
title: 解像度
topic: Scene7 Image Serving - Image Rendering API
uuid: b04b3746-90e6-4545-9c57-7ee3b61d99bf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 7%

---


# 解像度{#resolution}

初期設定の解像度。 特定のカタログレコードに有効なcatalog::Resolution値が含まれていない場合にデフォルトの解像度を指定します。

## プロパティ {#section-06d519158b9f479896f945747c670736}

0より大きい実数。 通常はピクセル/インチで表されますが、他の単位（ピクセル/メートルなど）でも使用できます。

## 初期設定 {#section-eea922c37c224e1dbcab3bc53ee13aca}

定義されていない場合や空の場合は`default::Resolution`から継承されます。

## 関連項目 {#section-fa286e5440f04d0aa07c7326cc0d72f1}

[catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7) ,  [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)
