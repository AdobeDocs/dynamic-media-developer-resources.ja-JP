---
description: ユーザー属性（名前、電子メール、役割など）を設定します。
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
TQID: 'https://experienceleague.adobe.com/JzJv4nEeWfbY-Wp-qkEq883dlTqaRm9Fc-UvDa70dOg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 114
ht-degree: 14%

---

# setUserInfo{#setuserinfo}

ユーザー属性（名前、電子メール、役割など）を設定します。

構文

## 承認済みユーザータイプ {#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-71b457921fe74acb862a1e112e550211}

**入力（setUserInfoParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| userHANDLE | `xsd:string` | いいえ | ユーザーハンドル： |
| firstName | `xsd:string` | はい | 名。 |
| lastName | `xsd:string` | はい | 姓： |
| 電子メール | `xsd:string` | はい | ユーザーメール： |
| defaultRole | `xsd:string` | はい | ユーザーが属する各会社におけるユーザーの役割を設定します。 ただし、`IpsAdmin`の役割は、会社ごとの他の設定よりも優先されます。 |
| passwordExpires | `xsd:dateTime` | いいえ | パスワードの有効期限を設定します。 |
| isValid | `xsd:boolean` | はい | ユーザーが有効なIPS ユーザーであるかどうかを判断します。 |
| membershipArray | `types:CompanyMembershipUpdateArray` | はい | 企業が処理する一連の処理です。 |

**出力（setUserInfoReturn）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-272c103076fb4de0a53729e2f6bfb895}

**リクエスト**

```java
<setUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <firstName>test</firstName>
   <lastName>test</lastName>
   <email>test@test.test</email>
   <defaultRole>IpsAdmin</defaultRole>
   <isValid>true</isValid>
</setUserInfoParam>
```

**応答**

なし

