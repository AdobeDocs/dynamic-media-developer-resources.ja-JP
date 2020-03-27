---
description: 住所フィルター要素。 <rule>要素のオプションです。 ルールが適用されるときに、属性ClientAddressFilterを上書きします。
seo-description: 住所フィルター要素。 <rule>要素のオプションです。 ルールが適用されるときに、属性ClientAddressFilterを上書きします。
seo-title: addressfilter
solution: Experience Manager
title: addressfilter
topic: Scene7 Image Serving - Image Rendering API
uuid: e5702c6e-a49c-4da6-a29c-26e16bfdcad1
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# addressfilter{#addressfilter}

住所フィルター要素。 要素のオプシ `<rule>` ョンです。 ルールの適用時に、attribute::ClientAddressFilterを上書きします。

## Attributes {#section-e7a0960f7f0045da91de37824aa4aeaa}

なし

## データ {#section-eb138f192516418a9ef2ab9a38c9ee9e}

IPアドレスのコンマ区切りリスト。 個々のアドレスには、IPアドレス範囲を指定できるオプションのネットマスクサフィックスを含めることができます。 詳しくは、を ` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)` 参照してください。

## 説明 {#section-099b7839c4be40c68cbff29dad14e7d5}

この画像カタログへのアクセスは、要素で指定することで、1つ以上の特定のIPアドレスに制限で `<addressfilter>` きます。 クライアントのIPアドレスが一致しない場合、「要求が拒否されました」エラーがクライアントに返されます。

が空の場合、または指定されていな `<addressfilter>` い場合、アクセスは制限されません。

要素内のが `<expression>` 存在しな `<rule>` いか空の場合は、すべてのリクエ `<addressfilter>` ストに適用されます。

`localhost` は、明示的に指定されていない場合でも、常に `ClientAddressFilter` 定義の暗黙的な部分です。 指定に関係なく、 `localhost` からの要求は拒否されることはあり `ClientAddressFilter` ません。

## SeeaAlso {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
