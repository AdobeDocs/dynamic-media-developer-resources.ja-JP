---
description: ユーザー属性（名前、Eメール、役割など）を
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 16%

---

# setUserInfo{#setuserinfo}

ユーザー属性（名前、Eメール、役割など）を

構文

## 許可されたユーザーの種類 {#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-71b457921fe74acb862a1e112e550211}

**入力(setUserInfoParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | いいえ | ユーザーハンドル。 |
| `*`firstName`*` | `xsd:string` | はい | 名。 |
| `*`lastName`*` | `xsd:string` | はい | 姓。 |
| `*`電子メール`*` | `xsd:string` | はい | ユーザーの電子メール。 |
| `*`defaultRole`*` | `xsd:string` | はい | 所属する各会社のユーザーの役割を設定します。 ただし、`IpsAdmin`の役割は、他の会社ごとの設定よりも優先されます。 |
| `*`passwordExpires`*` | `xsd:dateTime` | いいえ | パスワードの有効期限を設定します。 |
| `*`isValid`*` | `xsd:boolean` | はい | ユーザーが有効なIPSユーザーかどうかを判断します。 |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | はい | 会社が処理する配列。 |

**出力(setUserInfoReturn)**

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
