---
description: クライアントIPアドレスフィルタ。 1つ以上のIPアドレスまたはアドレス範囲を指定できます。
seo-description: クライアントIPアドレスフィルタ。 1つ以上のIPアドレスまたはアドレス範囲を指定できます。
seo-title: ClientAddressFilter
solution: Experience Manager
title: ClientAddressFilter
topic: Scene7 Image Serving - Image Rendering API
uuid: b68f527b-7fa7-43e3-9517-57a6c3700b06
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 2%

---


# ClientAddressFilter{#clientaddressfilter}

クライアントIPアドレスフィルタ。 1つ以上のIPアドレスまたはアドレス範囲を指定できます。

指定した場合、リストにないIPアドレスのクライアントからのこの画像カタログへの要求は拒否されます。 `localhost` は、明示的に指定されていない場合でも、常に `ClientAddressFilter` 定義の暗黙的な部分です。`localhost`からの要求は、`ClientAddressFilter`仕様に関係なく拒否されません。

## プロパティ {#section-21a2992f108d42fb8660c0d65aa61e13}

IPアドレスとオプションのネットマスクを含むコンマ区切りリスト（[CIDR表記](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation)を使用）:

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* IPアドレス( *[!DNL ddd.ddd.ddd.ddd]* 形式)

* *[!DNL netmask]* ネットマスク(0...32)

`<addressfilter>`要素を含む前処理ルールが適用される場合、この属性は無視されます。

## 初期設定 {#section-beddaa18ed6c4f3ba1eb2d4471267712}

定義されていない場合や空の場合は`default::AddressFilter`から継承されます。

## 例 {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* アクセス制限なし：`0.0.0.0/0`
* `192: 192.0.0.0/8`で始まるすべてのアドレスへのアクセスを許可する
* `192.168.12.0`と`192.168.13.255: 192.168.12.0/23`の間のアドレスを持つ512ホストへのアクセスを許可する

* 単一のIPアドレスへのアクセスを許可する：`192.168.2.117`または`192.168.2.117/32`

## 関連項目 {#section-6198780c7b3045aabd211eefb38bc565}

[addressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
