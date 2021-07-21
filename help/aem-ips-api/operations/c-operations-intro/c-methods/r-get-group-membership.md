---
description: グループのメンバーを返します。
solution: Experience Manager
title: getGroupMembership
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 847e4982-219d-47fd-b94c-f7d520ba1367
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 18%

---

# getGroupMembership{#getgroupmembership}

グループのメンバーを返します。

構文

## 許可されたユーザーの種類 {#section-35d070e5c4d74ca69df508368953cfb8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-2e92f850254e46e48403acaa215341a5}

**入力(getGroupMembershipParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | いいえ | ユーザーへのハンドル。 |
| `*`companyHandle`*` | `xsd:string` | いいえ | 会社の取っ手。 |

**出力(getGroupMembershipReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`groupArray`*` | `types:GroupArray` | はい | グループの配列。 |

## 例 {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

このコードサンプルは、グループのすべてのメンバーを返します。 会社とユーザーのハンドルはオプションなので、この操作はすべてのグループのすべてのメンバーを返すことができます。

**リクエスト**

```java
<ns1:getGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupMembershipParam>
```

**応答**

```java
<getGroupMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle><companyHandle>47</companyHandle><name>MyGroup</name><isSystemDefined>false</isSystemDefined></items></groupArray></getGroupMembershipReturn>
```
