---
description: '[イメージレンダリング]は、ビネット内のグループまたはオブジェクトにマテリアルを適用します。'
solution: Experience Manager
title: 資料
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# 資料{#materials}

[イメージレンダリング]は、ビネット内のグループまたはオブジェクトにマテリアルを適用します。

マテリアルは、*属性*&#x200B;のセットで構成されます。 一部の属性は、特定の材料に必要なものと、オプションのもの、存在する場合は無視されるものがあります。 多くの属性にはデフォルト値があります。 すべてのマテリアルをすべてのオブジェクトに適用できるわけではありません（例えば、キャビネットマテリアルをソファに適用できないなど）。

MSS(Material Specification Segment)内で発生するが、上記または以下の特定のマテリアル・テーブルに記載されていない属性は、サーバによって無視されます。

次の表に、基本的なマテリアル属性を示します。 IRは、[高度なレンダリング効果](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281)を制御する追加の属性をサポートします。

特に断りのない限り、材料属性はすべてオプションで、適切なデフォルト値を持ちます。

* [べた塗り](r-ir-solid-colors.md)
* [繰り返し可能なテクスチャ](r-ir-repeatable-textures.md)
* [壁境界](r-ir-wall-borders.md)
* [デカル](r-ir-decals.md)
* [キャビネット](r-ir-cabinets.md)
* [窓の表紙](r-ir-window-coverings.md)
