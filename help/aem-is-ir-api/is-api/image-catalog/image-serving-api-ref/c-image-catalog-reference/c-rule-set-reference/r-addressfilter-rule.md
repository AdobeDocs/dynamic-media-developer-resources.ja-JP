---
description: アドレスフィルタ要素。 <rule>要素と<pathrule>要素のオプションです。
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: fe5df3a8-c9b2-4fad-ab9f-ca0b06016faf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 4%

---

# addressfilter{#addressfilter}

アドレスフィルタ要素。 `<rule>`要素と`<pathrule>`要素でオプションです。

ルールが適用されると、`attribute::ClientAddressFilter`を上書きします。

## 属性 {#section-31e9ad29e9934933ac154bccbc729172}

なし

## データ {#section-c762bdfe425140d689ea5abf25e9a48a}

IPアドレスのコンマ区切りリスト。 個々のアドレスには、IPアドレス範囲を指定できるように、オプションのネットマスクサフィックスを含めることができます。 詳細は`attribute::ClientAddressFilter`を参照。

## 説明 {#section-d561b2485e004ef8a2085997d0f4bca6}

`<addressfilter>`要素で指定すると、この画像カタログへのアクセスを1つ以上の特定のクライアントIPアドレスに制限できます。 クライアントのIPアドレスが一致しない場合、「リクエストが拒否されました」エラーがクライアントに返されます。

`<addressfilter>`が空の場合や指定されていない場合は、アクセスは制限されません。

`<rule>`要素内の`<expression>`がない場合や空の場合は、すべてのリクエストに`<addressfilter>`が適用されます。

## 関連項目 {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
