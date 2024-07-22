---
description: ユーザーに関する情報を取得します。 リクエストを承認するための認証情報として、システムユーザーのメールアドレスとパスワードを使用します。 それ以外の場合、操作はデフォルトユーザーに関する情報を取得します。
solution: Experience Manager
title: getUserinfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1981f25f-779e-4434-ab6b-0debb40521fe
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 10%

---

# getUserinfo{#getuserinfo}

ユーザーに関する情報を取得します。 リクエストを承認するための認証情報として、システムユーザーのメールアドレスとパスワードを使用します。 それ以外の場合、操作はデフォルトユーザーに関する情報を取得します。

構文

## 許可されているユーザータイプ {#section-1c42d78e914a4b84a946b3480f29b36a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-e87b3cb743494719925c9458eed433b6}

**入力（getUserInfoParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| userHandle | `xsd:string` | いいえ | 戻す情報を持つユーザーを表すハンドル。 |
| 電子メール | `xsd:string` | いいえ | ユーザーのメールアドレス。 |

**出力（getUserInfoReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| userInfo | `types:User` | はい | ユーザーの名、姓、メールアドレス、役割、およびユーザーが有効かどうか、ユーザーのパスワードの有効期限がいつ切れるか。 |

## 例 {#section-98d77a2e360a438dbe240099bea26a65}

このコードサンプルでは、デフォルトの IPS ユーザーの情報を返します。

**リクエスト**

```java
<getUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd" /></getUserInfoParam>
```

**応答**

```java
<ns1:getUserInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
   <ns1:userInfo> 
      <ns1:userHandle>3261|user@scene7.com</ns1:userHandle> 
      <ns1:firstName>FirstName</ns1:firstName> 
      <ns1:lastName>LastName</ns1:lastName> 
      <ns1:email>user@scene7.com</ns1:email> 
      <ns1:role>IpsAdmin</ns1:role> 
      <ns1:isValid>true</ns1:isValid> 
      <ns1:passwordExpires>2107-04-22T18:35:41.995Z</ns1:passwordExpires> 
   </ns1:userInfo> 
</ns1:getUserInfoReturn>
```
