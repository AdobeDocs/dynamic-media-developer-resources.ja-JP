---
description: 住所フィルター要素。 <rule>要素と<pathrule>要素のオプションです。
seo-description: 住所フィルター要素。 <rule>要素と<pathrule>要素のオプションです。
seo-title: addressfilter
solution: Experience Manager
title: addressfilter
topic: Scene7 Image Serving - Image Rendering API
uuid: 677eb19f-fd1a-4f74-8d55-6045baf01bf5
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# addressfilter{#addressfilter}

住所フィルター要素。 および要素のオ `<rule>` プショ `<pathrule>` ンです。

ルールが `attribute::ClientAddressFilter` 適用された場合に上書きされます。

## Attributes {#section-31e9ad29e9934933ac154bccbc729172}

なし

## データ {#section-c762bdfe425140d689ea5abf25e9a48a}

IPアドレスのコンマ区切りリスト。 個々のアドレスには、IPアドレス範囲を指定できるオプションのネットマスクサフィックスを含めることができます。 詳しくは、を `attribute::ClientAddressFilter` 参照してください。

## 説明 {#section-d561b2485e004ef8a2085997d0f4bca6}

この画像カタログへのアクセスは、要素で指定することで、1つ以上の特定のクライアントIPアドレスに制限で `<addressfilter>` きます。 クライアントのIPアドレスが一致しない場合、「要求が拒否されました」エラーがクライアントに返されます。

が空の場合、または指定されていな `<addressfilter>` い場合、アクセスは制限されません。

要素内のが `<expression>` 存在しな `<rule>` いか空の場合は、すべてのリクエ `<addressfilter>` ストに適用されます。

## 関連項目 {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
