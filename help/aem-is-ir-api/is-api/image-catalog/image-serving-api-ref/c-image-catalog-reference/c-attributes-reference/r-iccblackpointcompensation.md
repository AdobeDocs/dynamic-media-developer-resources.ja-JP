---
description: ブラックポイント補正。 icc=で明示的な選択が行われない場合に、ブラックポイント補正をカラー変換に適用するかどうかを指定します。
solution: Experience Manager
title: IccBlackPointCompensation
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9cf6a415-cc82-40e9-a8b9-a687ca95560e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 4%

---

# IccBlackPointCompensation{#iccblackpointcompensation}

ブラックポイント補正。 icc=で明示的な選択が行われない場合に、ブラックポイント補正をカラー変換に適用するかどうかを指定します。

## プロパティ {#section-ea27b8089b89468bbc38e9e7154ea413}

フラグ。 0 に設定すると無効になり、1 に設定するとブラックポイント補正が有効になります。

## 初期設定 {#section-0d79b203be4c434f927b7c03c7a0062d}

定義されていない場合または空の場合は `default::IccBlackPointCompensation` から継承します。

## 関連項目 {#section-c6ae25de4b5b45dcb068340acfee91be}

[attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) &#42;, [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
