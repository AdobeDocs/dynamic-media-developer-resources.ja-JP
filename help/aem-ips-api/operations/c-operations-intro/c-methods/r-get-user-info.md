---
description: ユーザーに関する情報を取得します。 リクエストを承認するための資格情報として、システムユーザーのメールアドレスとパスワードを使用します。 それ以外の場合、操作はデフォルトユーザーに関する情報を取得します。
solution: Experience Manager
title: getUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1981f25f-779e-4434-ab6b-0debb40521fe
TQID: 'https://experienceleague.adobe.com/4FEwXXgelDJ5CDf4FhaE11GS3vsnZi6wjY7HproyCIw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 139
ht-degree: 10%

---

# getUserInfo{#getuserinfo}

ユーザーに関する情報を取得します。 リクエストを承認するための資格情報として、システムユーザーのメールアドレスとパスワードを使用します。 それ以外の場合、操作はデフォルトユーザーに関する情報を取得します。

構文

## 承認済みユーザータイプ {#section-1c42d78e914a4b84a946b3480f29b36a}

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
| userHANDLE | `xsd:string` | いいえ | 情報を返すユーザーに対して処理します。 |
| 電子メール | `xsd:string` | いいえ | ユーザーのメールアドレス： |

**出力（getUserInfoReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| userInfo | `types:User` | はい | ユーザーの名前、姓、メールアドレス、役割、およびユーザーが有効かどうか、ユーザーのパスワードの有効期限はいつか。 |

## 例 {#section-98d77a2e360a438dbe240099bea26a65}

このコードサンプルは、デフォルトのIPS ユーザーの情報を返します。

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

