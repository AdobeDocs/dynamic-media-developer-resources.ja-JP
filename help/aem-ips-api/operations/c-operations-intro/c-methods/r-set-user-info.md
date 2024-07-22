---
description: ユーザー属性（名前、メール、役割など）を設定します。
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 14%

---

# setUserInfo{#setuserinfo}

ユーザー属性（名前、メール、役割など）を設定します。

構文

## 許可されているユーザータイプ {#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-71b457921fe74acb862a1e112e550211}

**入力（setUserInfoParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| userHandle | `xsd:string` | いいえ | ユーザーハンドル。 |
| firstName | `xsd:string` | はい | 名。 |
| lastName | `xsd:string` | はい | 姓。 |
| 電子メール | `xsd:string` | はい | ユーザーのメール。 |
| defaultRole | `xsd:string` | はい | ユーザーが属する各会社のユーザーの役割を設定します。 ただし、`IpsAdmin` の役割は、会社ごとのその他の設定を上書きします。 |
| passwordExpires | `xsd:dateTime` | いいえ | のパスワードの有効期限を設定します。 |
| isValid | `xsd:boolean` | はい | ユーザーが有効な IPS ユーザーかどうかを判断します。 |
| membershipArray | `types:CompanyMembershipUpdateArray` | はい | 会社ハンドルの配列。 |

**出力（setUserInfoReturn）**

IPS API は、この操作に対して応答を返しません。

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
