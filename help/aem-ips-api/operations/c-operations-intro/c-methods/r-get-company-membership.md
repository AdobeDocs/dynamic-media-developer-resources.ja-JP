---
description: 会社配列内のユーザーのメンバーシップを取得します。
solution: Experience Manager
title: getCompanyMembership
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 17%

---


# getCompanyMembership{#getcompanymembership}

会社配列内のユーザーのメンバーシップを取得します。

構文

## 認証済みユーザータイプ{#section-f8bba547e1f648648be99dc48fd72b5d}

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

## パラメータ {#section-8745c360c3e1400a88e9bdb26bcb93de}

**入力(getCompanyMembershipParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | いいえ | メンバーシップを取得するユーザーのハンドル。 |

**Output (getCompanyMembershipReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`membershipArray`*` | `types:CompanyMembershipArray` | はい | 会社メンバーシップの配列。 |

## 例 {#section-e4958d104ea344a4a79f57d07b46eba7}

このコードの例では、ユーザーハンドルを使用して、配列内のユーザーの会社メンバーシップをすべて取得します。 応答は簡潔にするために切り捨てられました。

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

