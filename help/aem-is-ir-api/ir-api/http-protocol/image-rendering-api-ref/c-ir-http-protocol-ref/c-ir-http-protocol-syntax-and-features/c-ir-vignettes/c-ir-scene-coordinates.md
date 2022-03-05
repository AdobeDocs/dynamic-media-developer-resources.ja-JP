---
title: シーンの座標
description: シーンの座標空間は、テクスチャ可能なオブジェクトサーフェス上でのサイズと距離を指定するために使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: de7f088e-3825-4d2e-924e-001a44db62a0
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 1%

---

# シーンの座標{#scene-coordinates}

シーンの座標空間は、テクスチャ可能なオブジェクトサーフェス上でのサイズと距離を指定するために使用します。

ほとんどのビネットは物理的なオブジェクトを表す実世界のシーンなので、ほとんどのビネットはシーンの座標空間の単位としてインチを使用して作成されます。 その他の単位（mm や cm など）も使用できます。 画像レンダリングは、単位の変換をサポートしていません。

次のコマンドは、シーン座標空間の値を受け付けます。

* [グラウト=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
* [pos=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8)
* [サイズ=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988)
