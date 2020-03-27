---
description: 特定の会社（ハンドルで識別）のユーザー、電子メールアドレス、パスワードを持つユーザーがログインできるかどうかを確認します。
seo-description: 特定の会社（ハンドルで識別）のユーザー、電子メールアドレス、パスワードを持つユーザーがログインできるかどうかを確認します。
seo-title: checkLogin
solution: Experience Manager
title: checkLogin
topic: Scene7 Image Production System API
uuid: 69f9e5f6-50c2-403d-93b2-b84a01f512a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# checkLogin{#checklogin}

特定の会社（ハンドルで識別）のユーザー、電子メールアドレス、パスワードを持つユーザーがログインできるかどうかを確認します。

>[!NOTE]
>
>会社のハンドルを省略した場合、このメソッドはデフォルトユーザーのログインを確認します。

## 認証されたユーザータイプ {#section-df8b26b550854f899948276adaca083a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-1ad4c0b4803b4388aedd655030676cb3}

**入力(checkLoginParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | いいえ | ユーザーを含む会社のハンドル。 |
| ` *`電子メール`*` | `xsd:string` | はい | ユーザーの電子メールアドレス。 |
| ` *`パスワード`*` | `xsd:string` | はい | ユーザーのパスワード。 |

**出力(checkLoginParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`status`*` | `xsd:string` | はい | ユーザーのログインステータス。 |

## 例 {#section-23f90100a9d94bc7b4045634cccd1b98}

このサンプルコードでは、会社のハンドルパラメータ、電子メールアドレス、およびパスワードを使用して、ユーザがIPSにログインできるかどうかを判断します。 ユーザーがログ *インで* きる場合は、文字列、を返します `ValidLogin`。 ユーザーがログ *インできな* い場合は、文字列、を返します `InvalidLogin`。

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

