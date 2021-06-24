---
description: 特定の会社（ハンドルで識別）、電子メールアドレス、パスワードを持つユーザーがログインできるかどうかを確認します。
solution: Experience Manager
title: checkLogin
feature: Dynamic Media Classic、SDK/API
role: Developer,Administrator
exl-id: 1f96f376-574c-464b-9c89-c215f6454b81
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 12%

---

# checkLogin{#checklogin}

特定の会社（ハンドルで識別）、電子メールアドレス、パスワードを持つユーザーがログインできるかどうかを確認します。

>[!NOTE]
>
>会社の処理を省略した場合、このメソッドはデフォルトユーザーのログインを確認します。

## 許可されたユーザーの種類 {#section-df8b26b550854f899948276adaca083a}

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
| `*`companyHandle`*` | `xsd:string` | いいえ | ユーザーを含む会社へのハンドル。 |
| `*`電子メール`*` | `xsd:string` | はい | ユーザーの電子メールアドレス。 |
| `*`パスワード`*` | `xsd:string` | はい | ユーザーのパスワード。 |

**出力(checkLoginParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`status`*` | `xsd:string` | はい | ユーザーのログインステータス。 |

## 例 {#section-23f90100a9d94bc7b4045634cccd1b98}

このサンプルコードでは、会社のハンドルパラメータ、電子メールアドレス、およびパスワードを使用して、ユーザーがIPSにログインできるかどうかを判断します。 ユーザー&#x200B;*が*&#x200B;ログインできる場合、このメソッドは文字列`ValidLogin`を返します。 ユーザー&#x200B;*がログインできない*&#x200B;場合、このメソッドは文字列`InvalidLogin`を返します。

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
