---
description: グループのメンバーを返します。
solution: Experience Manager
title: getGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 847e4982-219d-47fd-b94c-f7d520ba1367
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 16%

---

# getGroupMembers{#getgroupmembership}

グループのメンバーを返します。

構文

## 許可されているユーザータイプ {#section-35d070e5c4d74ca69df508368953cfb8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-2e92f850254e46e48403acaa215341a5}

**入力（getGroupMembershipParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| userHandle | `xsd:string` | いいえ | ユーザーへのハンドル。 |
| companyHandle | `xsd:string` | いいえ | 会社へのハンドル。 |

**出力（getGroupMembershipReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| groupArray | `types:GroupArray` | はい | グループの配列。 |

## 例 {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

このコードサンプルは、グループのすべてのメンバーを返します。 会社およびユーザーハンドルはオプションなので、操作は、すべてのグループのすべてのメンバーを返すことができます。

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
