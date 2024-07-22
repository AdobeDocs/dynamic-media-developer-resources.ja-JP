---
description: 特定の会社（ハンドルで識別）、メールアドレスおよびパスワードを持つユーザーがログインできるかどうかを確認します。
solution: Experience Manager
title: checkLogin
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f96f376-574c-464b-9c89-c215f6454b81
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 11%

---

# checkLogin{#checklogin}

特定の会社（ハンドルで識別）、メールアドレスおよびパスワードを持つユーザーがログインできるかどうかを確認します。

>[!NOTE]
>
>会社ハンドルが省略された場合、このメソッドはデフォルトユーザーのログインをチェックします。

## 許可されているユーザータイプ {#section-df8b26b550854f899948276adaca083a}

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
| 電子メール | `xsd:string` | はい | ユーザーの E メールアドレス。 |
| パスワード | `xsd:string` | はい | ユーザーのパスワード。 |

**出力（checkLoginParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| status | `xsd:string` | はい | ユーザーのログインステータス。 |

## 例 {#section-23f90100a9d94bc7b4045634cccd1b98}

このサンプルコードでは、会社のハンドルパラメーター、メールアドレスおよびパスワードを使用して、ユーザーが IPS にログインできるかどうかを判断します。 ユーザー *can* がログインすると、このメソッドは文字列 `ValidLogin` を返します。 ユーザー *ログインできない* 場合、このメソッドは文字列 `InvalidLogin` を返します。

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
