---
description: カラー変換レンダリングの方法。 icc=でレンダリングインテントが指定されていない場合の、カラー変換のデフォルトのレンダリングインテントを提供します。
solution: Experience Manager
title: IccRenderIntent
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 732b1935-6556-4420-a056-4e00cb3ed152
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---

# IccRenderIntent{#iccrenderintent}

カラー変換レンダリングの方法。 icc=でレンダリングインテントが指定されていない場合の、カラー変換のデフォルトのレンダリングインテントを提供します。

## プロパティ {#section-2540099fb2fc47d29b04642da4f5922a}

列挙 知覚的には0、相対的な色域を維持するには1、彩度には2、絶対的な色域を維持するには3に設定します。

## 初期設定 {#section-61a05067905b44099c228e15de279dbd}

`default::IccRenderIntent`から継承されます（定義されていない場合または空の場合）。

## 関連項目 {#section-7da9ff3038ca452a9f7375a1ca0581af}

[attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)  *,  [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f),  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
