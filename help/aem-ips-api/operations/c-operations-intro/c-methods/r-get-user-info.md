---
description: ユーザーに関する情報を取得します。 要求を認証するための資格情報として、システムユーザーの電子メールアドレスとパスワードを使用します。 それ以外の場合は、操作はデフォルトのユーザーに関する情報を取得します。
solution: Experience Manager
title: getUserInfo
feature: Dynamic Media Classic、SDK/API
role: Developer,Administrator
exl-id: 1981f25f-779e-4434-ab6b-0debb40521fe
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 11%

---

# getUserInfo{#getuserinfo}

ユーザーに関する情報を取得します。 要求を認証するための資格情報として、システムユーザーの電子メールアドレスとパスワードを使用します。 それ以外の場合は、操作はデフォルトのユーザーに関する情報を取得します。

構文

## 許可されたユーザーの種類 {#section-1c42d78e914a4b84a946b3480f29b36a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-e87b3cb743494719925c9458eed433b6}

**入力(getUserInfoParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | いいえ | 情報を返すユーザーに対して処理を行います。 |
| `*`電子メール`*` | `xsd:string` | いいえ | ユーザーの電子メールアドレス。 |

**出力(getUserInfoReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`userInfo`*` | `types:User` | はい | ユーザーの名、姓、電子メールアドレス、役割、およびユーザーが有効かどうか、およびユーザーのパスワードの期限が切れたとき。 |

## 例 {#section-98d77a2e360a438dbe240099bea26a65}

このコードサンプルは、デフォルトのIPSユーザの情報を返します。

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
