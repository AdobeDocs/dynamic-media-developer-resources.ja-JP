---
description: 会社ハンドルで指定された会社のユーザーを返します。
seo-description: 会社ハンドルで指定された会社のユーザーを返します。
seo-title: getCompanyMembers
solution: Experience Manager
title: getCompanyMembers
uuid: 45e2d040-a70a-46f4-863a-633ddabcbcf6
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 14%

---


# getCompanyMembers{#getcompanymembers}

会社ハンドルで指定された会社のユーザーを返します。

構文

## 認証済みユーザータイプ{#section-b2bc2fa0cc944cea8be82524838307cc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-5602e4d6f2214e398e6a804e61f1a088}

**入力(getCompanyMembersParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | メンバーを取得する会社のハンドル。 |
| `*`includeInvalid`*` | `xsd:boolean` | はい | 無効な会社を含めます。 |

**出力(getCompanyMembersReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`memberArray`*` | `types:CompanyMemberArray` | はい | ユーザーメンバーシップの配列。 |

## 例 {#section-39d8cf3653fd4fe8b842caabac9dedfc}

次のコードのサンプルを使用すると、会社のすべてのメンバーがユーザー配列で返されます。 応答は簡潔にするために切り捨てられました。

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

