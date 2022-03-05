---
title: 資料
description: '[ イメージレンダリング ] は、ビネット内のグループまたはオブジェクトにマテリアルを適用します。'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# 資料{#materials}

[ イメージレンダリング ] は、ビネット内のグループまたはオブジェクトにマテリアルを適用します。

マテリアルは、 *属性*. 一部の属性は、特定の材料に対して必要なものや、オプションの属性、存在する場合は無視される属性があります。 多くの属性にはデフォルト値があります。 すべてのマテリアルをすべてのオブジェクトに適用できるわけではありません（たとえば、キャビネットのマテリアルをソファに適用することはできません）。

MSS(Material Specification Segment) 内で発生するが、上記または以下の特定の材料テーブルにリストされていない属性は、サーバーでは無視されます。

次の表に、基本的なマテリアル属性を示します。 IR は、制御用の追加の属性をサポートします [高度なレンダリング効果](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

特に断りのない限り、すべてのマテリアル属性はオプションで、適切なデフォルト値を持ちます。

* [べた塗り](r-ir-solid-colors.md)
* [繰り返し可能なテクスチャ](r-ir-repeatable-textures.md)
* [壁の境界](r-ir-wall-borders.md)
* [デカル](r-ir-decals.md)
* [キャビネット](r-ir-cabinets.md)
* [ウィンドウカバリング](r-ir-window-coverings.md)
