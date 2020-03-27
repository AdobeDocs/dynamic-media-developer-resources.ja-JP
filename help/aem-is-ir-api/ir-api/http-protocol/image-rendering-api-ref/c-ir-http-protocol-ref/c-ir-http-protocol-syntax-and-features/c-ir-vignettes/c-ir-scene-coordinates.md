---
description: シーン座標空間は、テクスチャ可能なオブジェクトサーフェス上のサイズと距離を指定するために使用されます。
seo-description: シーン座標空間は、テクスチャ可能なオブジェクトサーフェス上のサイズと距離を指定するために使用されます。
seo-title: シーンの座標
solution: Experience Manager
title: シーンの座標
topic: Scene7 Image Serving - Image Rendering API
uuid: d1215ba2-9cad-4cf6-a57e-7c1d845b0199
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# シーンの座標{#scene-coordinates}

シーン座標空間は、テクスチャ可能なオブジェクトサーフェス上のサイズと距離を指定するために使用されます。

ほとんどのビネットは物理オブジェクトを表す実世界のシーンなので、ほとんどのビネットはシーンの座標空間の単位としてインチを使用して作成されます。 その他の単位（mmやcmなど）も使用できます。 画像レンダリングは単位の変換をサポートしていません。

次の各コマンドは、シーン座標空間の値を受け取ります。

* [グラウト=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
* [pos=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8)
* [サイズ=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988)

