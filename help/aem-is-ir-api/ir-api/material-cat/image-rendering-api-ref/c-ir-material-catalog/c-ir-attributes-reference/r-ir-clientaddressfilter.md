---
description: クライアントのIPアドレスフィルター。 1つ以上のIPアドレスまたはアドレス範囲を指定できます。
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# ClientAddressFilter{#clientaddressfilter}

クライアントのIPアドレスフィルター。 1つ以上のIPアドレスまたはアドレス範囲を指定できます。

指定した場合、登録されていないIPアドレスのクライアントからのこの画像カタログへの要求は拒否されます。 `localhost` は、明示的に指定されていない場合で `ClientAddressFilter` も、常に暗黙的に定義の一部です。`localhost`からの要求は、`ClientAddressFilter`仕様に関係なく、拒否されることはありません。

## プロパティ {#section-21a2992f108d42fb8660c0d65aa61e13}

オプションのネットマスクを含むIPアドレスのコンマ区切りリスト（[CIDR表記](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation)を使用）:

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* 形式のIPアド *[!DNL ddd.ddd.ddd.ddd]* レス

* *[!DNL netmask]* ネットマスク(0...32)

`<addressfilter>`要素を含む前処理ルールが適用される場合、この属性は無視されます。

## 初期設定 {#section-beddaa18ed6c4f3ba1eb2d4471267712}

`default::AddressFilter`から継承されます（定義されていない場合または空の場合）。

## 例 {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* アクセス制限なし：`0.0.0.0/0`
* `192: 192.0.0.0/8`で始まるすべてのアドレスへのアクセスを許可する
* `192.168.12.0`と`192.168.13.255: 192.168.12.0/23`の間のアドレスを持つ512ホストへのアクセスを許可する

* 単一のIPアドレスへのアクセス権の付与：`192.168.2.117`または`192.168.2.117/32`

## 関連項目 {#section-6198780c7b3045aabd211eefb38bc565}

[addressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
