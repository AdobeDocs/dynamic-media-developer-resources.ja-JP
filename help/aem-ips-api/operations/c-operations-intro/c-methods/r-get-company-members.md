---
description: 会社ハンドルで指定された会社のユーザーを返します。
solution: Experience Manager
title: getCompanyMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da5e5a48-2e0b-4ccc-a71e-b5b746484d4a
TQID: 'https://experienceleague.adobe.com/QMJGqj7IEplTMdFFwVP3UReZAJsi25tHaaMewM30MSU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 89
ht-degree: 14%

---

# getCompanyMembers{#getcompanymembers}

会社ハンドルで指定された会社のユーザーを返します。

構文

## 承認済みユーザータイプ {#section-b2bc2fa0cc944cea8be82524838307cc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-5602e4d6f2214e398e6a804e61f1a088}

**入力（getCompanyMembersParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 取得するメンバーの会社へのハンドル。 |
| includeInvalid | `xsd:boolean` | はい | 無効な会社を含めます。 |

**出力（getCompanyMembersReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| memberArray | `types:CompanyMemberArray` | はい | ユーザーメンバーシップの配列。 |

## 例 {#section-39d8cf3653fd4fe8b842caabac9dedfc}

このコードのサンプルは、会社のすべてのメンバーをユーザー配列内に返します。 応答は簡潔にするために省略されています。

**リクエスト**

```java
<ns1:getCompanyMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeInvalid>false</ns1:includeInvalid>
</ns1:getCompanyMembersParam>
```

**応答**

```java
<getCompanyMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray>
      <items>
         <userHandle>66|pbayol@adobe.com</userHandle>
         <firstName>Peter</firstName>
         <lastName>Bayol</lastName>
         <email>pbayol@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-25T23:12:49.472-07:00</passwordExpires>
      </items>
      ...
   </memberArray>
</getCompanyMembersReturn>
```

