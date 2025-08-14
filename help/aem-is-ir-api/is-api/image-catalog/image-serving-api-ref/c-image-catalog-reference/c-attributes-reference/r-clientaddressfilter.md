---
description: クライアントの IP アドレスフィルター。 1 つ以上の IP アドレスまたはアドレスの範囲を指定できます。
solution: Experience Manager
title: Client アドレス フィルター
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 028cef35-2862-452c-872c-b953e8ccb195
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# Client アドレス フィルター{#clientaddressfilter}

クライアントの IP アドレスフィルター。 1 つ以上の IP アドレスまたはアドレスの範囲を指定できます。

指定した場合、リストにない IP アドレスのクライアントから作成されるこの画像カタログへのリクエストは拒否されます。

## プロパティ {#section-d785265988324af68835410c9ba54147}

オプションのネットマスクを使用した IP アドレスのコンマ区切りリスト （CIDR 表記が使用されています）:

`*`ipAddress`*` `[`/ *`netmask`*`]`&#42; `[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p>IP アドレス <span class="varname">ddd.ddd.ddd.ddd</span> 形式です。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ネットマスク </span> </p></td> 
  <td class="stentry"> <p>ネットマスク（0...32）。 </p></td> 
 </tr> 
</table>

`<addressfilter>` 要素を含む前処理ルールが適用される場合、この属性は無視されます。

## 初期設定 {#section-de26e8c9225745e985e4beac1f03f4f6}

定義されていない場合または空の場合は `default::AddressFilter` から継承します。

## 例 {#section-a955314d2b6a4213a16c12a8b18d8627}

アクセス制限なし：`0.0.0.0/0`

192 以降のすべてのアドレスへのアクセスを許可：`192.0.0.0/8`

192.168.12.0 ～ 192.168.13.255 のアドレスを持つ 512 ホストへのアクセスを許可：`192.168.12.0/23`

単一の IP アドレスにアクセスを許可：`192.168.2.117` または `192.168.2.117/32`

## 関連項目 {#section-4ea89a7d82e14a4a800487d2d8801465}

[addressfilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
