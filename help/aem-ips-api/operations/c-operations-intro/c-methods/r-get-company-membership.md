---
description: ユーザーのメンバーシップを会社配列で取得します。
solution: Experience Manager
title: getCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 53af8a97-208c-4c44-93d6-aa36a459af51
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 14%

---

# getCompanyMembership{#getcompanymembership}

ユーザーのメンバーシップを会社配列で取得します。

構文

## 許可されているユーザータイプ {#section-f8bba547e1f648648be99dc48fd72b5d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-8745c360c3e1400a88e9bdb26bcb93de}

**入力（getCompanyMembershipParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| userHandle | `xsd:string` | いいえ | メンバーシップを取得するユーザーへのハンドル。 |

**出力（getCompanyMembershipReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| membershipArray | `types:CompanyMembershipArray` | はい | 会社のメンバーシップの配列。 |

## 例 {#section-e4958d104ea344a4a79f57d07b46eba7}

このコードサンプルでは、ユーザーハンドルを取得し、配列でユーザーのすべての会社メンバーシップを取得します。 簡潔にするために、応答は切り捨てられました。

**リクエスト**

```java
<ns1:getCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
</ns1:getCompanyMembershipParam>
```

**応答**

```java
<getCompanyMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <membershipArray>
      <items>
         <companyHandle>48</companyHandle>
         <name>AIR</name>
         <rootPath>AIR/</rootPath>
         <expires>2101-01-31T23:00:00.485-08:00</expires>
      </items>
      ...
    </membershipArray>
</getCompanyMembershipReturn>
```
