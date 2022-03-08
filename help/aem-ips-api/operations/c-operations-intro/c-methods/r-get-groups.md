---
description: 会社グループを返します。
solution: Experience Manager
title: getGroups
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d98c08a6-4c20-4538-9598-c905078ab7de
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 22%

---

# getGroups{#getgroups}

会社グループを返します。

構文

## 認証済みユーザータイプ {#section-27c77680a2f34e2f9ecd0af4ebb6847e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-0e06195f23dd4c69922df210f566dd18}

**入力 (getGroupsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社への取り扱い。 |

**出力 (getGroupsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| groupArray | `types:GroupArray` | はい | グループの配列。 |

## 例 {#section-ed0708f611574354bf0c6ea83912b531}

このコードは、特定の会社に属するすべてのグループと、各グループに関する特定の情報を含む配列を返します。

**リクエスト**

```java
<ns1:getGroupsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupsParam>
```

```java
<getGroupsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle>
         <companyHandle>47</companyHandle>
         <name>MyGroup</name>
         <isSystemDefined>false</isSystemDefined>
      </items>
   </groupArray>
</getGroupsReturn>
```
