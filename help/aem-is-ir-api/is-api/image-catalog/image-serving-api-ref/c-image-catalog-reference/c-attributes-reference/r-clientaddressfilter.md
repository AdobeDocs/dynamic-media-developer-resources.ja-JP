---
description: クライアントのIPアドレスフィルター。 1つ以上のIPアドレスまたはアドレス範囲を指定できます。
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 028cef35-2862-452c-872c-b953e8ccb195
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---

# ClientAddressFilter{#clientaddressfilter}

クライアントのIPアドレスフィルター。 1つ以上のIPアドレスまたはアドレス範囲を指定できます。

指定した場合、登録されていないIPアドレスのクライアントからのこの画像カタログへの要求は拒否されます。

## プロパティ {#section-d785265988324af68835410c9ba54147}

オプションのネットマスクを含むIPアドレスのコンマ区切りリスト（CIDR表記を使用）:

`*`ipAddress`*` `[`/  *`netmask`*`]`*  `[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p><span class="varname"> ddd.ddd.ddd.ddd</span>形式のIPアドレス。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> netmask</span> </p></td> 
  <td class="stentry"> <p>ネットマスク(0...32)。 </p></td> 
 </tr> 
</table>

`<addressfilter>`要素を含む前処理ルールが適用される場合、この属性は無視されます。

## 初期設定 {#section-de26e8c9225745e985e4beac1f03f4f6}

`default::AddressFilter`から継承されます（定義されていない場合または空の場合）。

## 例 {#section-a955314d2b6a4213a16c12a8b18d8627}

アクセス制限なし：`0.0.0.0/0`

192以降のすべてのアドレスに対するアクセス権を付与する：`192.0.0.0/8`

192.168.12.0～192.168.13.255のアドレスを持つ512ホストに対するアクセス権を付与：`192.168.12.0/23`

単一のIPアドレスへのアクセス権の付与：`192.168.2.117`または`192.168.2.117/32`

## 関連項目 {#section-4ea89a7d82e14a4a800487d2d8801465}

[addressfilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
