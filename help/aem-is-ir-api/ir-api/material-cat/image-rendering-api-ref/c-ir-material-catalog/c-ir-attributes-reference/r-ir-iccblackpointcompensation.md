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

## プロパティ {#section-21fd20b16bea4a22aecab0ae8b81e332}

フラグ。 0に設定すると無効になり、1に設定するとブラックポイントの補正が有効になります。

## 初期設定 {#section-5bc6703a43a149f18af88b70baae568f}

定義されていない場合や空の場合は`default::IccBlackPointCompensation`から継承されます。

## 関連項目 {#section-90fcbddf02c54846aa09f85fabc7b4d4}

[attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
