---
title: IccBlackPointCompensation
description: ブラックポイント補正。 icc=で明示的な選択が行われない場合に、ブラックポイント補正をカラー変換に適用するかどうかを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9d075434-5ef0-4b6a-ad24-1ef9c57e3e47
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 4%

---

# IccBlackPointCompensation{#iccblackpointcompensation}

ブラックポイント補正。 `icc=` で明示的な選択が行われない場合に、黒点補正をカラー変換に適用するかどうかを指定します。

## プロパティ {#section-21fd20b16bea4a22aecab0ae8b81e332}

フラグ。 `0` に設定するとブラックポイント補正が無効になり、`1` に設定するとブラックポイント補正が有効になります。

## 初期設定 {#section-5bc6703a43a149f18af88b70baae568f}

定義されていない場合または空の場合は `default::IccBlackPointCompensation` から継承します。

## 関連項目 {#section-90fcbddf02c54846aa09f85fabc7b4d4}

[attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
