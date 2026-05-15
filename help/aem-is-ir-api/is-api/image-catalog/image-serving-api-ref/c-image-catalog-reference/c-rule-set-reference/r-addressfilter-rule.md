---
description: アドレスフィルター要素。 <rule>および<pathrule>要素のオプション。
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe5df3a8-c9b2-4fad-ab9f-ca0b06016faf
TQID: 'https://experienceleague.adobe.com/NkzpvFZFbluayVtCa7qBVcSgY2aU5N7R2-rZkQCZHkw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 3%

---

# addressfilter{#addressfilter}

アドレスフィルター要素。 `<rule>`要素と`<pathrule>`要素ではオプションです。

ルールが適用されるときに`attribute::ClientAddressFilter`を上書きします。

## 属性 {#section-31e9ad29e9934933ac154bccbc729172}

なし

## データ {#section-c762bdfe425140d689ea5abf25e9a48a}

IP アドレスのコンマ区切りリスト。 個々のアドレスごとにオプションのネットマスクサフィックスを含めて、IP アドレス範囲を指定できます。 詳しくは、`attribute::ClientAddressFilter`を参照してください。

## 説明 {#section-d561b2485e004ef8a2085997d0f4bca6}

この画像カタログへのアクセスは、`<addressfilter>`要素で指定することで、1つ以上の特定のクライアント IP アドレスに制限できます。 クライアントのIP アドレスが一致しない場合、「リクエスト拒否」エラーがクライアントに返されます。

`<addressfilter>`が空であるか指定されていない場合、アクセスは制限されません。

`<rule>`要素の`<expression>`が存在しないか空の場合、`<addressfilter>`はすべてのリクエストに適用されます。

## 関連項目 {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
