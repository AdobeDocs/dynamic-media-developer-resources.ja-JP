---
description: 会社の配列内のユーザーのメンバーシップを取得します。
seo-description: 会社の配列内のユーザーのメンバーシップを取得します。
seo-title: getCompanyMembership
solution: Experience Manager
title: getCompanyMembership
topic: Scene7 Image Production System API
uuid: fb3dfe29-4292-4ab2-8015-36c4930a9c05
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getCompanyMembership{#getcompanymembership}

会社の配列内のユーザーのメンバーシップを取得します。

構文

## 認証されたユーザータイプ {#section-f8bba547e1f648648be99dc48fd72b5d}

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
| ` *`userHandle`*` | `xsd:string` | いいえ | メンバーシップを取得するユーザーのハンドル。 |

**Output (getCompanyMembershipReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`membershipArray`*` | `types:CompanyMembershipArray` | はい | 会社のメンバーシップの配列。 |

## 例 {#section-e4958d104ea344a4a79f57d07b46eba7}

このコード例では、ユーザーが処理し、すべてのユーザーの会社メンバーシップを配列で取得します。 応答は簡潔にするために切り捨てられました。

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

