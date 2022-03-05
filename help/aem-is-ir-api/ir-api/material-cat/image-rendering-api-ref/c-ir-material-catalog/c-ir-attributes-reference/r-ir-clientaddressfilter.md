---
description: クライアント IP アドレスフィルター。 1 つ以上の IP アドレスまたはアドレス範囲を指定できます。
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---

# ClientAddressFilter{#clientaddressfilter}

クライアント IP アドレスフィルター。 1 つ以上の IP アドレスまたはアドレス範囲を指定できます。

指定した場合、登録されていない IP アドレスのクライアントから派生するこの画像カタログへの要求は拒否されます。 `localhost` は常に暗黙的に `ClientAddressFilter` 定義（明示的に指定されていない場合も含む） からのリクエスト `localhost` は、 `ClientAddressFilter` 仕様。

## プロパティ {#section-21a2992f108d42fb8660c0d65aa61e13}

オプションのネットマスク ([CIDR 表記](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) が使用されています )。

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* IP アドレス： *[!DNL ddd.ddd.ddd.ddd]* 形式

* *[!DNL netmask]* ネットマスク (0...32)

この属性は、 `<addressfilter>` 要素が適用されます。

## 初期設定 {#section-beddaa18ed6c4f3ba1eb2d4471267712}

継承元 `default::AddressFilter` が定義されていない場合、または空の場合は。

## 例 {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* アクセス制限なし： `0.0.0.0/0`
* で始まるすべてのアドレスへのアクセス権を付与する `192: 192.0.0.0/8`
* アドレスを持つ 512 ホストに対するアクセスを許可する `192.168.12.0` および `192.168.13.255: 192.168.12.0/23`

* 単一の IP アドレスへのアクセスを許可する： `192.168.2.117` または `192.168.2.117/32`

## 関連項目 {#section-6198780c7b3045aabd211eefb38bc565}

[addressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
