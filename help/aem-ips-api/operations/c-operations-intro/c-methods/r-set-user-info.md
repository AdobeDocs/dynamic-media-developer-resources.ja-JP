---
description: ユーザー属性（名前、電子メール、役割など）を設定します。
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 16%

---


# setUserInfo{#setuserinfo}

ユーザー属性（名前、電子メール、役割など）を設定します。

構文

## 認証済みユーザータイプ{#section-6c28db5d15b3449492a73749e4f981ac}

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
| `*`defaultRole`*` | `xsd:string` | はい | 所属する各会社のユーザーの役割を設定します。 ただし、`IpsAdmin`役割は、会社ごとの他の設定よりも優先されます。 |
| `*`passwordExpires`*` | `xsd:dateTime` | いいえ | パスワードの有効期限を設定します。 |
| `*`isValid`*` | `xsd:boolean` | はい | ユーザが有効なIPSユーザであるかどうかを判定します。 |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | はい | 会社ハンドルの配列。 |

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
