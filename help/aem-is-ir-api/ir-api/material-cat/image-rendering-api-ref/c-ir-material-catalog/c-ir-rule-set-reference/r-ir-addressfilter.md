---
description: アドレスフィルター要素。 <rule>要素ではオプションです。 ルールが適用されるときに、属性ClientAddressFilterを上書きします。
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
TQID: 'https://experienceleague.adobe.com/583zFF80AMZnaF4C-RQpRQI684hRlPRCuwoMPHGJ6eg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 150
ht-degree: 1%

---

# addressfilter{#addressfilter}

アドレスフィルター要素。 `<rule>`要素ではオプションです。 ルールが適用されたときに属性：:ClientAddressFilterを上書きします。

## 属性 {#section-e7a0960f7f0045da91de37824aa4aeaa}

なし

## データ {#section-eb138f192516418a9ef2ab9a38c9ee9e}

IP アドレスのコンマ区切りリスト。 個々のアドレスごとにオプションのネットマスクサフィックスを含めて、IP アドレス範囲を指定できます。 詳しくは、[attribute::ClientAddressFilter](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md)を参照してください。

## 説明 {#section-099b7839c4be40c68cbff29dad14e7d5}

この画像カタログへのアクセスは、`<addressfilter>`要素で指定することで、1つ以上の特定のIP アドレスに制限できます。 クライアントのIP アドレスが一致しない場合、「リクエスト拒否」エラーがクライアントに返されます。

`<addressfilter>`が空であるか指定されていない場合、アクセスは制限されません。

`<rule>`要素の`<expression>`が存在しないか空の場合、`<addressfilter>`はすべてのリクエストに適用されます。

`localhost`は、明示的に指定されていない場合でも、常に暗黙的に`ClientAddressFilter`定義の一部になります。 `ClientAddressFilter`の仕様に関係なく、`localhost`からのリクエストは拒否されません。

## SeeaAlso {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)

