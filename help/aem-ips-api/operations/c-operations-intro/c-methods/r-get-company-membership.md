---
description: ユーザーのメンバーシップを企業配列で取得します。
solution: Experience Manager
title: getCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 53af8a97-208c-4c44-93d6-aa36a459af51
TQID: 'https://experienceleague.adobe.com/h-fjzt4o5zdyVkWh9pkWDLs6KXTF3--s4koIQv77Zno'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 14%

---

# getCompanyMembership{#getcompanymembership}

ユーザーのメンバーシップを企業配列で取得します。

構文

## 承認済みユーザータイプ {#section-f8bba547e1f648648be99dc48fd72b5d}

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
| userHANDLE | `xsd:string` | いいえ | メンバーシップを取得するユーザーへのハンドル。 |

**出力（getCompanyMembershipReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| membershipArray | `types:CompanyMembershipArray` | はい | 企業のメンバーシップの配列。 |

## 例 {#section-e4958d104ea344a4a79f57d07b46eba7}

このコードサンプルは、ユーザーハンドルを取り出し、ユーザーのすべての会社メンバーシップを配列で取得します。 応答は簡潔にするために省略されています。

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
