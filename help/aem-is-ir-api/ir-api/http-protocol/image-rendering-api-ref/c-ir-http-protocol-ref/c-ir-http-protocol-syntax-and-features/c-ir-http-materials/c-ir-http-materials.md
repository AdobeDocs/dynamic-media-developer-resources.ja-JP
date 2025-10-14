---
title: 素材
description: イメージ レンダリングは、ビネット内のグループまたはオブジェクトにマテリアルを適用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# 素材{#materials}

イメージ レンダリングは、ビネット内のグループまたはオブジェクトにマテリアルを適用します。

マテリアルは、一連の *属性* で構成されます。 特定のマテリアルに必須の属性もあれば、オプションの属性もあり、存在する場合は無視される属性もあります。 多くの属性にはデフォルト値があります。 すべてのマテリアルがすべてのオブジェクトに適用できるわけではありません（たとえば、キャビネット マテリアルはソファに適用できません）。

材料仕様セグメント （MSS）内に存在するが、上または下の特定の材料表にリストされていない属性は、サーバーによって無視されます。

次の表に、基本的な材料属性を示します。 赤外線は、制御する追加のアトリビュート [&#x200B; 高度なレンダリング エフェクト &#x200B;](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281) をサポートします。

特に明記されていない限り、すべてのマテリアル属性はオプションで、適切な既定値が設定されています。

* [単色](r-ir-solid-colors.md)
* [反復可能なテクスチャ](r-ir-repeatable-textures.md)
* [壁の境界](r-ir-wall-borders.md)
* [デカール](r-ir-decals.md)
* [キャビネット](r-ir-cabinets.md)
* [窓の覆い](r-ir-window-coverings.md)
