---
description: ブラックポイントの補正。 icc=で明示的な選択が行われない場合に、ブラックポイント補正をカラー変換に適用するかどうかを指定します。
solution: Experience Manager
title: IccBlackPointCompensation
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---


# IccBlackPointCompensation{#iccblackpointcompensation}

ブラックポイントの補正。 icc=で明示的な選択が行われない場合に、ブラックポイント補正をカラー変換に適用するかどうかを指定します。

## プロパティ {#section-ea27b8089b89468bbc38e9e7154ea413}

フラグ。 0に設定すると無効になり、1に設定するとブラックポイントの補正が有効になります。

## 初期設定 {#section-0d79b203be4c434f927b7c03c7a0062d}

定義されていない場合や空の場合は`default::IccBlackPointCompensation`から継承されます。

## 関連項目 {#section-c6ae25de4b5b45dcb068340acfee91be}

[attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) *,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
