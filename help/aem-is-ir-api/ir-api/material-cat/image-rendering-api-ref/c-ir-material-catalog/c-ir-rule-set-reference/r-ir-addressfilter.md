---
description: アドレスフィルタ要素。 <rule>要素のオプションです。 ルールが適用されると、属性ClientAddressFilterが上書きされます。
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 1%

---

# addressfilter{#addressfilter}

アドレスフィルタ要素。 `<rule>`要素ではオプションです。 ルールが適用されると、attribute::ClientAddressFilterが上書きされます。

## 属性 {#section-e7a0960f7f0045da91de37824aa4aeaa}

なし

## データ {#section-eb138f192516418a9ef2ab9a38c9ee9e}

IPアドレスのコンマ区切りリスト。 個々のアドレスには、IPアドレス範囲を指定できるように、オプションのネットマスクサフィックスを含めることができます。 詳細は` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)`を参照。

## 説明 {#section-099b7839c4be40c68cbff29dad14e7d5}

`<addressfilter>`要素で指定すると、この画像カタログへのアクセスを1つ以上の特定のIPアドレスに制限できます。 クライアントのIPアドレスが一致しない場合、「リクエストが拒否されました」エラーがクライアントに返されます。

`<addressfilter>`が空の場合や指定されていない場合は、アクセスは制限されません。

`<rule>`要素内の`<expression>`がない場合や空の場合は、すべてのリクエストに`<addressfilter>`が適用されます。

`localhost` は、明示的に指定されていない場合で `ClientAddressFilter` も、常に暗黙的に定義の一部です。`localhost`からの要求は、`ClientAddressFilter`仕様に関係なく、拒否されることはありません。

## SeeaAlso {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
