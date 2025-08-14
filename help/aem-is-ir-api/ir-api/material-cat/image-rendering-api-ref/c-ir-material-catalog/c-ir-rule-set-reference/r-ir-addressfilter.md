---
description: アドレスフィルター要素。 <rule> 要素内ではオプションです。 ルールが適用されると、属性 ClientAddressFilter を上書きします。
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 1%

---

# addressfilter{#addressfilter}

アドレスフィルター要素。 `<rule>` 要素ではオプションです。 ルールが適用されると、attribute::ClientAddressFilter を上書きします。

## 属性 {#section-e7a0960f7f0045da91de37824aa4aeaa}

なし

## データ {#section-eb138f192516418a9ef2ab9a38c9ee9e}

IP アドレスのコンマ区切りリスト。 個々のアドレスには、IP アドレス範囲の指定を可能にするオプションのネットマスクサフィックスを含めることができます。 詳しくは、[attribute::ClientAddressFilter](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md) を参照してください。

## 説明 {#section-099b7839c4be40c68cbff29dad14e7d5}

`<addressfilter>` 要素で指定することで、この画像カタログへのアクセスを 1 つ以上の特定の IP アドレスに制限できます。 クライアントの IP アドレスが一致しない場合は、「request refused」エラーがクライアントに返されます。

`<addressfilter>` が空であるか、指定されていない場合、アクセスは制限されません。

`<expression>` 要素の `<rule>` が存在しないか空の場合、`<addressfilter>` はすべてのリクエストに適用されます。

`localhost` は、明示的に指定されない場合でも、常に `ClientAddressFilter` 定義の暗黙的な一部となります。 `localhost` からのリクエストは、`ClientAddressFilter` の仕様に関係なく、拒否されません。

## SeeAlso {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
