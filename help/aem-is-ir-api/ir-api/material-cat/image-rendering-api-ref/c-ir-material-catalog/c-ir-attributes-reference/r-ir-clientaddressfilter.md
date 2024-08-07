---
title: Client アドレス フィルター
description: クライアントの IP アドレスフィルター。 1 つ以上の IP アドレスまたはアドレスの範囲を指定できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# Client アドレス フィルター{#clientaddressfilter}

クライアントの IP アドレスフィルター。 1 つ以上の IP アドレスまたはアドレスの範囲を指定できます。

指定した場合、登録されていない IP アドレスのクライアントからこの画像カタログへのリクエストは拒否されます。 `localhost` は、明示的に指定されない場合でも、常に `ClientAddressFilter` 定義の暗黙的な一部となります。 `localhost` からのリクエストは、`ClientAddressFilter` の仕様に関係なく、拒否されません。

## プロパティ {#section-21a2992f108d42fb8660c0d65aa61e13}

オプションのネットマスクを使用した IP アドレスのコンマ区切りリスト （[CIDR 表記 ](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) が使用されています）:

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ddd.ddd.ddd.ddd]* 形式の *[!DNL ipAddress]* IP アドレス

* *[!DNL netmask]* ネットマスク （0...32）

`<addressfilter>` 要素を含む前処理ルールが適用される場合、この属性は無視されます。

## 初期設定 {#section-beddaa18ed6c4f3ba1eb2d4471267712}

定義されていない場合または空の場合は `default::AddressFilter` から継承します。

## 例 {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* アクセス制限なし：`0.0.0.0/0`
* `192: 192.0.0.0/8` で始まるすべてのアドレスにアクセス権を付与します
* `192.168.12.0` ～ `192.168.13.255: 192.168.12.0/23` のアドレスを持つ 512 ホストへのアクセスを許可します。

* 単一の IP アドレスにアクセスを許可：`192.168.2.117` または `192.168.2.117/32`

## 関連項目 {#section-6198780c7b3045aabd211eefb38bc565}

[addressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
