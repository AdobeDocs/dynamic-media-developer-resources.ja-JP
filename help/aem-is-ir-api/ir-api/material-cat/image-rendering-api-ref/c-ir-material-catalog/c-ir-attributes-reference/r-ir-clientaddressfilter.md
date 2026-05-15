---
title: ClientAddressFilter
description: クライアント IP アドレス フィルター。 1つ以上のIP アドレスまたはアドレス範囲を指定できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
TQID: 'https://experienceleague.adobe.com/azMITpRcITTOEB0FCev6vWiTmocumP-0HTQD3rIV-fA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 156
ht-degree: 2%

---

# ClientAddressFilter{#clientaddressfilter}

クライアント IP アドレス フィルター。 1つ以上のIP アドレスまたはアドレス範囲を指定できます。

指定すると、リストに登録されていないIP アドレスのクライアントから送信されたこの画像カタログへのリクエストは拒否されます。 `localhost`は、明示的に指定されていない場合でも、常に暗黙的に`ClientAddressFilter`定義の一部になります。 `ClientAddressFilter`の仕様に関係なく、`localhost`からのリクエストは拒否されません。

## プロパティ {#section-21a2992f108d42fb8660c0d65aa61e13}

オプションのネットマスクを含むIP アドレスのコンマ区切りリスト （[CIDR表記法](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation)を使用）:

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ddd.ddd.ddd.ddd]*&#x200B;形式の&#x200B;*[!DNL ipAddress]* IP アドレス

* *[!DNL netmask]* ネットマスク （0...32）

この属性は、`<addressfilter>`要素を持つ前処理ルールが適用される場合は無視されます。

## 初期設定 {#section-beddaa18ed6c4f3ba1eb2d4471267712}

定義されていない場合や空の場合は、`default::AddressFilter`から継承されます。

## 例 {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* アクセス制限がありません：`0.0.0.0/0`
* `192: 192.0.0.0/8`で始まるすべてのアドレスにアクセス権を付与
* アドレスが`192.168.12.0`から`192.168.13.255: 192.168.12.0/23`までの512 ホストへのアクセス権を付与します

* 1つのIP アドレスへのアクセス権の付与：`192.168.2.117`または`192.168.2.117/32`

## 関連項目 {#section-6198780c7b3045aabd211eefb38bc565}

[addressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
