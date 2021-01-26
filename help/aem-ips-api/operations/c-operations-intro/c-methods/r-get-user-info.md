---
description: ユーザーに関する情報を取得します。 要求を承認するための資格情報として、システムユーザーの電子メールアドレスとパスワードを使用します。 それ以外の場合は、デフォルトユーザーに関する情報が取得されます。
seo-description: ユーザーに関する情報を取得します。 要求を承認するための資格情報として、システムユーザーの電子メールアドレスとパスワードを使用します。 それ以外の場合は、デフォルトユーザーに関する情報が取得されます。
seo-title: getUserInfo
solution: Experience Manager
title: getUserInfo
topic: Dynamic Media Image Production System API
uuid: b305c108-22e9-4268-a5b3-25fddd844c24
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 9%

---


# getUserInfo{#getuserinfo}

ユーザーに関する情報を取得します。 要求を承認するための資格情報として、システムユーザーの電子メールアドレスとパスワードを使用します。 それ以外の場合は、デフォルトユーザーに関する情報が取得されます。

構文

## 認証済みユーザータイプ{#section-1c42d78e914a4b84a946b3480f29b36a}

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
| `*`userHandle`*` | `xsd:string` | いいえ | 情報を返すユーザーのハンドル。 |
| `*`電子メール`*` | `xsd:string` | いいえ | ユーザーの電子メールアドレス。 |

**出力(getUserInfoReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`userInfo`*` | `types:User` | はい | ユーザーの名、姓、電子メールアドレス、役割、およびユーザーが有効かどうか、およびユーザーのパスワードが期限切れになったとき。 |

## 例 {#section-98d77a2e360a438dbe240099bea26a65}

次のコードサンプルは、既定のIPSユーザの情報を返します。

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

