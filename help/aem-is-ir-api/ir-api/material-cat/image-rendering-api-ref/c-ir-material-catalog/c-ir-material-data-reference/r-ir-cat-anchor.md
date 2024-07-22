---
description: 画像アンカー。 繰り返し可能なテクスチャ、壁の境界、またはデカール イメージのアンカーポイント（ホットスポット）を指定します。
solution: Experience Manager
title: アンカー
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1336330e-86e5-418d-bea3-0c09368e3528
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 3%

---

# アンカー{#anchor}

画像アンカー。 繰り返し可能なテクスチャ、壁の境界、またはデカール イメージのアンカーポイント（ホットスポット）を指定します。

繰り返し可能なテクスチャがビネットオブジェクトに適用され、テクスチャのアンカーポイントがオブジェクトのテクスチャ原点に配置されます。 デカル転写イメージは、オブジェクトのデカル原点にデカル アンカー点が配置されるように、ビネット オブジェクトに適用されます。 壁の境界には、x 値のみが使用され、y 値は無視されます。

## プロパティ {#section-bc4bc8b897c64535b88681e57d72942f}

コンマで区切られた 2 つの整数。 画像の左上隅を基準としたピクセルオフセット。 ソリッド カラーおよびキャビネット マテリアルで `catalog::Alignment=3` 成されている場合は無視されます。

## 初期設定 {#section-b7ccc419a356415294706cd295ae96c9}

フィールドが空か、または存在しない場合は、繰り返し可能なテクスチャ マテリアルのイメージの左上隅（0,0）が使用され、デカル マテリアルの場合はイメージの中心が使用されます。

## 関連項目 {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[catalog::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
