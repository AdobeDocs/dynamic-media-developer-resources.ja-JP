---
title: 解像度
description: デフォルトの解像度。 特定のカタログレコードに有効なカタログ解像度の値が含まれていない場合に使用する、デフォルトの解像度を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd47f41a-b527-4c78-afb5-b9e9af0868cc
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 6%

---

# 解像度{#resolution}

デフォルトの解像度。 特定のカタログレコードに有効な `catalog::Resolution` 値が含まれていない場合のデフォルトの解決方法を指定します。

## プロパティ {#section-06d519158b9f479896f945747c670736}

`0` より大きい実数。 通常は 1 インチあたりのピクセル数で表しますが、1 メートルあたりのピクセル数など、他の単位の場合もあります。

## 初期設定 {#section-eea922c37c224e1dbcab3bc53ee13aca}

定義されていない場合または空の場合は `default::Resolution` から継承します。

## 関連項目 {#section-fa286e5440f04d0aa07c7326cc0d72f1}

[catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7) , [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)
