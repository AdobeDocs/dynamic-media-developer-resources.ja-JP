---
description: アドレスフィルター要素。 <rule>要素のオプションです。 ルールが適用される場合に、属性ClientAddressFilterを上書きします。
seo-description: アドレスフィルター要素。 <rule>要素のオプションです。 ルールが適用される場合に、属性ClientAddressFilterを上書きします。
seo-title: addressfilter
solution: Experience Manager
title: addressfilter
topic: Scene7 Image Serving - Image Rendering API
uuid: e5702c6e-a49c-4da6-a29c-26e16bfdcad1
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 1%

---


# addressfilter{#addressfilter}

アドレスフィルター要素。 `<rule>`要素のオプションです。 ルールが適用される場合、attribute::ClientAddressFilterを上書きします。

## 属性{#section-e7a0960f7f0045da91de37824aa4aeaa}

なし

## データ {#section-eb138f192516418a9ef2ab9a38c9ee9e}

IPアドレスのカンマ区切りリスト。 個々のアドレスには、IPアドレスの範囲を指定できるように、オプションのネットマスクサフィックスを含めることができます。 詳細は` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)`を参照してください。

## 説明 {#section-099b7839c4be40c68cbff29dad14e7d5}

`<addressfilter>`要素で指定すると、この画像カタログへのアクセスを1つ以上の特定のIPアドレスに制限できます。 クライアントのIPアドレスが一致しない場合、「要求が拒否されました」エラーがクライアントに返されます。

`<addressfilter>`が空の場合、または指定されていない場合、アクセスは制限されません。

`<rule>`要素の`<expression>`が存在しない場合や空の場合は、`<addressfilter>`がすべてのリクエストに適用されます。

`localhost` は、明示的に指定されていない場合でも、常に `ClientAddressFilter` 定義の暗黙的な部分です。`localhost`からの要求は、`ClientAddressFilter`仕様に関係なく拒否されません。

## 参照{#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
