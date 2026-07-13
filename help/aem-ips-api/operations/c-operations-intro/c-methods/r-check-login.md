---
description: 特定の会社（ハンドルで識別）、メールアドレス、パスワードを持つユーザーがログインできるかどうかを確認します。
solution: Experience Manager
title: checkLogin
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f96f376-574c-464b-9c89-c215f6454b81
TQID: 'https://experienceleague.adobe.com/5o2geLVIOZLg7tmKrHueWkzjf4EhXedAJ5qvWxTzjB0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 145
ht-degree: 11%

---

# checkLogin{#checklogin}

特定の会社（ハンドルで識別）、メールアドレス、パスワードを持つユーザーがログインできるかどうかを確認します。

>[!NOTE]
>
>会社ハンドルが省略された場合、このメソッドはデフォルトのユーザーのログインを確認します。

## 承認済みユーザータイプ {#section-df8b26b550854f899948276adaca083a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-1ad4c0b4803b4388aedd655030676cb3}

**入力（checkLoginParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | いいえ | ユーザーを含む会社へのハンドル。 |
| 電子メール | `xsd:string` | はい | ユーザーのメールアドレス。 |
| パスワード | `xsd:string` | はい | ユーザーのパスワード。 |

**出力（checkLoginParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| status | `xsd:string` | はい | ユーザーのログインステータス。 |

## 例 {#section-23f90100a9d94bc7b4045634cccd1b98}

このサンプルコードでは、会社のハンドルパラメーター、電子メールアドレス、パスワードを使用して、ユーザーがIPSにログインできるかどうかを判断します。 ユーザー&#x200B;*can*&#x200B;がログインした場合、このメソッドは文字列`ValidLogin`を返します。 ユーザー&#x200B;*が*&#x200B;にログインできない場合、このメソッドは文字列`InvalidLogin`を返します。

**リクエスト**

```java
<ns1:checkLoginParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>137</ns1:companyHandle>
   <ns1:email>juser3@scene7.com</ns1:email>
   <ns1:password>welcome</ns1:password>
</ns1:checkLoginParam>
```

**応答**

```java
<ns1:checkLoginReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:status>InvalidLogin</ns1:status>
</ns1:checkLoginReturn>
```

