---
title: マテリアル
description: 画像レンダリングは、ビネット内のグループまたはオブジェクトにマテリアルを適用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
TQID: 'https://experienceleague.adobe.com/MNCMxRxVGLF2rsr7NsuTGLzWxM9zkR42MI9MLdaW6G8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 0%

---

# マテリアル{#materials}

画像レンダリングは、ビネット内のグループまたはオブジェクトにマテリアルを適用します。

マテリアルは、*属性*&#x200B;のセットで構成されます。 特定の材料に必要な属性もあれば、オプションの属性もあり、存在する場合は無視されます。 多くの属性にデフォルト値があります。 すべてのマテリアルをすべてのオブジェクトに適用できるわけではありません（たとえば、キャビネットのマテリアルをソファに適用することはできません）。

マテリアル仕様セグメント（MSS）内で発生するが、上記または以下の特定のマテリアルテーブルにリストされていない属性は、サーバーによって無視されます。

次の表に、基本的なマテリアル属性を示します。 IRでは、[高度なレンダリング効果](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281)を制御するための追加属性をサポートしています。

特に記載のない限り、すべてのマテリアル属性はオプションで、適切なデフォルト値を使用します。

* [べた塗](r-ir-solid-colors.md)
* [反復可能なテクスチャ](r-ir-repeatable-textures.md)
* [壁の境界線](r-ir-wall-borders.md)
* [デカール](r-ir-decals.md)
* [キャビネット](r-ir-cabinets.md)
* [ウィンドウのカバー](r-ir-window-coverings.md)

