---
description: 画像アンカー 繰り返し可能なテクスチャ、壁の境界、またはデカールのイメージのアンカーポイント（ホットスポット）を指定します。
seo-description: 画像アンカー 繰り返し可能なテクスチャ、壁の境界、またはデカールのイメージのアンカーポイント（ホットスポット）を指定します。
seo-title: アンカー
solution: Experience Manager
title: アンカー
topic: Scene7 Image Serving - Image Rendering API
uuid: 0b1a0fea-b299-44dc-b9fd-5916130b2ef3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 3%

---


# アンカー{#anchor}

画像アンカー 繰り返し可能なテクスチャ、壁の境界、またはデカールのイメージのアンカーポイント（ホットスポット）を指定します。

繰り返し可能なテクスチャは、ビネットオブジェクトに適用され、テクスチャアンカーポイントがオブジェクトのテクスチャ接触チャネルポイントに配置されます。 デカールのアンカーポイントがオブジェクトのデカール接触チャネルポイントに配置されるように、デカール画像がビネットオブジェクトに適用されます。 壁の境界では、xの値のみが使用されます。y値は無視されます。

## プロパティ {#section-bc4bc8b897c64535b88681e57d72942f}

カンマで区切られた2つの整数。 画像の左上隅を基準とするピクセルオフセット。 `catalog::Alignment=3`およびべた塗りのマテリアルとキャビネットマテリアルの場合は無視されます。

## 初期設定 {#section-b7ccc419a356415294706cd295ae96c9}

フィールドが空か存在しない場合は、繰り返し可能なテクスチャマテリアルのイメージの左上隅(0,0)が使用され、デカールマテリアルの場合はイメージの中心が使用されます。

## 関連項目 {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[catalog::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ,  [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
