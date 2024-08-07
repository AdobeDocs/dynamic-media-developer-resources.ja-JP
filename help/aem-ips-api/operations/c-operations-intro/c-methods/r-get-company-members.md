---
description: 会社ハンドルで指定された会社のユーザーを返します。
solution: Experience Manager
title: getCompanyMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da5e5a48-2e0b-4ccc-a71e-b5b746484d4a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 14%

---

# getCompanyMembers{#getcompanymembers}

会社ハンドルで指定された会社のユーザーを返します。

構文

## 許可されているユーザータイプ {#section-b2bc2fa0cc944cea8be82524838307cc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-5602e4d6f2214e398e6a804e61f1a088}

**入力（getCompanyMembersParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | メンバーを取得する会社へのハンドル。 |
| includeInvalid | `xsd:boolean` | はい | 無効な会社を含めます。 |

**出力（getCompanyMembersReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| memberArray | `types:CompanyMemberArray` | はい | ユーザーメンバーシップの配列。 |

## 例 {#section-39d8cf3653fd4fe8b842caabac9dedfc}

このコードサンプルでは、ユーザー配列内の会社のすべてのメンバーを返します。 簡潔にするために、応答は切り捨てられました。

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
