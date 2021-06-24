---
description: シーン座標空間は、テクスチャ可能なオブジェクトサーフェス上のサイズと距離を指定するために使用されます。
solution: Experience Manager
title: シーンの座標
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: de7f088e-3825-4d2e-924e-001a44db62a0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 1%

---

# シーンの座標{#scene-coordinates}

シーン座標空間は、テクスチャ可能なオブジェクトサーフェス上のサイズと距離を指定するために使用されます。

ほとんどのビネットは物理的なオブジェクトを表す実世界のシーンなので、ほとんどのビネットはシーンの座標空間の単位としてインチを使用して作成されます。 その他の単位（mmやcmなど）も使用できます。 画像レンダリングは単位変換をサポートしていません。

次のコマンドは、シーン座標空間の値を受け取ります。

* [グラウト=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
* [pos=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8)
* [サイズ=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988)
