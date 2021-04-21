---
description: ビネット内のグループまたはオブジェクトにマテリアルを適用します。
solution: Experience Manager
title: マテリアル
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# 材料{#materials}

ビネット内のグループまたはオブジェクトにマテリアルを適用します。

材料は、*属性*&#x200B;のセットで構成されます。 特定のマテリアルに必要な属性や、オプションの属性、および無視される属性があります。 多くの属性にはデフォルト値があります。 すべてのマテリアルをすべてのオブジェクトに適用できるわけではありません（例えば、キャビネットマテリアルをソファに適用できないなど）。

MSS(Material Specification Segment)内で発生し、上記または下記の特定の材料テーブルに記載されていない属性は、サーバーで無視されます。

次の表に、基本的なマテリアル属性をリストします。 IRは、[高度なレンダリング効果](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281)を制御する追加の属性をサポートします。

特に断りのない限り、マテリアル属性はすべてオプションで、適切なデフォルト値を持ちます。

* [べた塗り](r-ir-solid-colors.md)
* [繰り返し可能なテクスチャ](r-ir-repeatable-textures.md)
* [壁の境界](r-ir-wall-borders.md)
* [デカル](r-ir-decals.md)
* [キャビネット](r-ir-cabinets.md)
* [ウィンドウカバリング](r-ir-window-coverings.md)
