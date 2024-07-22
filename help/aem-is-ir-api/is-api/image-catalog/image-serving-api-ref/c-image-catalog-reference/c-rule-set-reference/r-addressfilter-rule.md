---
description: アドレスフィルター要素。 <rule> 要素および <pathrule> 要素内ではオプションです。
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe5df3a8-c9b2-4fad-ab9f-ca0b06016faf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 3%

---

# addressfilter{#addressfilter}

アドレスフィルター要素。 `<rule>` および `<pathrule>` 要素ではオプションです。

ルールが適用されると、`attribute::ClientAddressFilter` を上書きします。

## 属性 {#section-31e9ad29e9934933ac154bccbc729172}

なし

## データ {#section-c762bdfe425140d689ea5abf25e9a48a}

IP アドレスのコンマ区切りリスト。 個々のアドレスには、IP アドレス範囲の指定を可能にするオプションのネットマスクサフィックスを含めることができます。 詳細は、`attribute::ClientAddressFilter` を参照してください。

## 説明 {#section-d561b2485e004ef8a2085997d0f4bca6}

`<addressfilter>` 要素で指定することで、この画像カタログへのアクセスを 1 つ以上の特定のクライアント IP アドレスに制限できます。 クライアントの IP アドレスが一致しない場合は、「request refused」エラーがクライアントに返されます。

`<addressfilter>` が空であるか、指定されていない場合、アクセスは制限されません。

`<rule>` 要素の `<expression>` が存在しないか空の場合、`<addressfilter>` はすべてのリクエストに適用されます。

## 関連項目 {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
