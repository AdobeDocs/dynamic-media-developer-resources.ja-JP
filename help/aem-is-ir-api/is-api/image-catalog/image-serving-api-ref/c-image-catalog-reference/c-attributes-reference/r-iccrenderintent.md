---
description: カラー変換のマッチング方法。 icc=でレンダリングインテントが指定されていない場合のカラー変換の初期設定のマッチング方法を指定します。
seo-description: カラー変換のマッチング方法。 icc=でレンダリングインテントが指定されていない場合のカラー変換の初期設定のマッチング方法を指定します。
seo-title: IccRenderIntent
solution: Experience Manager
title: IccRenderIntent
topic: Scene7 Image Serving - Image Rendering API
uuid: c7edd8d8-c513-48d9-b3f6-1c3ad39a67e3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccRenderIntent{#iccrenderintent}

カラー変換のマッチング方法。 icc=でレンダリングインテントが指定されていない場合のカラー変換の初期設定のマッチング方法を指定します。

## プロパティ {#section-2540099fb2fc47d29b04642da4f5922a}

列挙。 知覚的には0、相対的な色域を維持するには1、彩度には2、絶対的な色域を維持するには3に設定します。

## 初期設定 {#section-61a05067905b44099c228e15de279dbd}

定義されていな `default::IccRenderIntent` い場合や空の場合に継承されます。

## 関連項目 {#section-7da9ff3038ca452a9f7375a1ca0581af}

[attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) *, [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
