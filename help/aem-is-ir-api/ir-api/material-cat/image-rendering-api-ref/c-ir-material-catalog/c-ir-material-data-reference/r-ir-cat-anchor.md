---
description: 画像アンカー。 繰り返し可能なテクスチャ、壁の境界、またはデカールイメージのアンカーポイント（ホットスポット）を指定します。
solution: Experience Manager
title: アンカー
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 1336330e-86e5-418d-bea3-0c09368e3528
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 3%

---

# アンカー{#anchor}

画像アンカー。 繰り返し可能なテクスチャ、壁の境界、またはデカールイメージのアンカーポイント（ホットスポット）を指定します。

繰り返し可能なテクスチャは、ビネットオブジェクトに適用され、テクスチャのアンカーポイントがオブジェクトのテクスチャの原点に配置されます。 デカールのアンカーポイントがオブジェクトのデカールの原点に配置されるように、デカールイメージがビネットオブジェクトに適用されます。 壁境界の場合は、x値のみが使用されます。y値は無視されます。

## プロパティ {#section-bc4bc8b897c64535b88681e57d72942f}

コンマで区切った2つの整数。 画像の左上隅を基準とするピクセルオフセット。 `catalog::Alignment=3`の場合は無視され、べた塗りとキャビネットのマテリアルで使用されます。

## 初期設定 {#section-b7ccc419a356415294706cd295ae96c9}

フィールドが空の場合や存在しない場合は、繰り返し可能なテクスチャマテリアルのイメージの左上コーナー(0,0)が使用されます。デカールマテリアルの場合は、イメージの中心が使用されます。

## 関連項目 {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[catalog::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) 、 [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
