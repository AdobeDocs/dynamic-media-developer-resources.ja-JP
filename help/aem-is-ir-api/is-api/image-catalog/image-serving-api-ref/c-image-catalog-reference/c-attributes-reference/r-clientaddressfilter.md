---
description: クライアント IP アドレス フィルター。 1つ以上のIP アドレスまたはアドレス範囲を指定できます。
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 028cef35-2862-452c-872c-b953e8ccb195
TQID: 'https://experienceleague.adobe.com/cQT0eRo0amqhX76H3dNZakwlGsKt3-MAkIsRZytyREI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 132
ht-degree: 3%

---

# ClientAddressFilter{#clientaddressfilter}

クライアント IP アドレス フィルター。 1つ以上のIP アドレスまたはアドレス範囲を指定できます。

指定すると、リストに登録されていないIP アドレスのクライアントから送信されたこの画像カタログへのリクエストは拒否されます。

## プロパティ {#section-d785265988324af68835410c9ba54147}

オプションのネットマスクを含むIP アドレスのコンマ区切りリスト（CIDR表記が使用されます）:

`*`ipAddress`*` `[`/ *`netmask`*`]`&#42; `[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p><span class="varname"> ddd.ddd.ddd.ddd</span>形式のIP アドレス。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ネットマスク </span> </p></td> 
  <td class="stentry"> <p>ネットマスク （0...32） </p></td> 
 </tr> 
</table>

この属性は、`<addressfilter>`要素を持つ前処理ルールが適用される場合は無視されます。

## 初期設定 {#section-de26e8c9225745e985e4beac1f03f4f6}

定義されていない場合や空の場合は、`default::AddressFilter`から継承されます。

## 例 {#section-a955314d2b6a4213a16c12a8b18d8627}

アクセス制限がありません：`0.0.0.0/0`

192以降のすべてのアドレスにアクセス権を付与する：`192.0.0.0/8`

アドレスが192.168.12.0から192.168.13.255までの512 ホストへのアクセス権を付与：`192.168.12.0/23`

1つのIP アドレスへのアクセス権の付与：`192.168.2.117`または`192.168.2.117/32`

## 関連項目 {#section-4ea89a7d82e14a4a800487d2d8801465}

[addressfilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
