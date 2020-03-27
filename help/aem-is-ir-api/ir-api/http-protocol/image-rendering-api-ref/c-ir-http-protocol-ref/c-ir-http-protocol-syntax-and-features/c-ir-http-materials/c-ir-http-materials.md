---
description: '[イメージレンダリング]は、ビネット内のグループまたはオブジェクトにマテリアルを適用します。'
seo-description: '[イメージレンダリング]は、ビネット内のグループまたはオブジェクトにマテリアルを適用します。'
seo-title: マテリアル
solution: Experience Manager
title: マテリアル
topic: Scene7 Image Serving - Image Rendering API
uuid: 82284e25-cfe0-4cf8-b410-b49196cc721c
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0

---


# マテリアル{#materials}

[イメージレンダリング]は、ビネット内のグループまたはオブジェクトにマテリアルを適用します。

マテリアルは属性のセットで構成さ *れます*。 一部のマテリアルには属性が必要で、その他の属性はオプションで、属性が存在する場合は無視されます。 多くの属性にはデフォルト値があります。 すべてのマテリアルをすべてのオブジェクトに適用できるわけではありません（例えば、キャビネットのマテリアルをソファに適用できないなど）。

材料仕様セグメント(MSS)内で発生し、上記または下記の特定の材料テーブルにリストされていない属性は、サーバーで無視されます。

次の表に、基本的なマテリアル属性を示します。 IRは、高度なレンダリング効果を制御する追加の [属性をサポートしま](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281)す。

特に断りのない限り、マテリアル属性はすべてオプションで、適切なデフォルト値を使用します。

* [べた塗り](r-ir-solid-colors.md)
* [繰り返し可能なテクスチャ](r-ir-repeatable-textures.md)
* [壁の境界](r-ir-wall-borders.md)
* [デカル](r-ir-decals.md)
* [キャビネット](r-ir-cabinets.md)
* [ウィンドウカバリング](r-ir-window-coverings.md)
