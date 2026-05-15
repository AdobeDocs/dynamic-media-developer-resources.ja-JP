---
description: 会社グループを返します。
solution: Experience Manager
title: getGroups
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d98c08a6-4c20-4538-9598-c905078ab7de
TQID: 'https://experienceleague.adobe.com/QyPdrXDIqo4P081BxGGFD-a53PcviQlNumVqwvEsNc8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 61
ht-degree: 19%

---

# getGroups{#getgroups}

会社グループを返します。

構文

## 承認済みユーザータイプ {#section-27c77680a2f34e2f9ecd0af4ebb6847e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-0e06195f23dd4c69922df210f566dd18}

**入力（getGroupsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社のハンドルです。 |

**出力（getGroupsReturn）**

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
