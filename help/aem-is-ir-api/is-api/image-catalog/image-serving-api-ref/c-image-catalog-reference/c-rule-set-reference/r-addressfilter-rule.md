---
description: アドレスフィルター要素。 <rule>要素と<pathrule>要素のオプションです。
solution: Experience Manager
title: addressfilter
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---


# addressfilter{#addressfilter}

アドレスフィルター要素。 `<rule>`要素と`<pathrule>`要素のオプションです。

ルールの適用時に`attribute::ClientAddressFilter`を上書きします。

## 属性{#section-31e9ad29e9934933ac154bccbc729172}

なし

## データ {#section-c762bdfe425140d689ea5abf25e9a48a}

IPアドレスのカンマ区切りリスト。 個々のアドレスには、IPアドレスの範囲を指定できるように、オプションのネットマスクサフィックスを含めることができます。 詳細は`attribute::ClientAddressFilter`を参照してください。

## 説明 {#section-d561b2485e004ef8a2085997d0f4bca6}

`<addressfilter>`要素で指定すると、この画像カタログへのアクセスを1つ以上の特定のクライアントIPアドレスに制限できます。 クライアントのIPアドレスが一致しない場合、「要求が拒否されました」エラーがクライアントに返されます。

`<addressfilter>`が空の場合、または指定されていない場合、アクセスは制限されません。

`<rule>`要素の`<expression>`が存在しない場合や空の場合は、`<addressfilter>`がすべてのリクエストに適用されます。

## 関連項目 {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
