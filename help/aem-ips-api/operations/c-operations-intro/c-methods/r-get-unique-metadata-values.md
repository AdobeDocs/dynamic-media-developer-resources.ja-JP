---
description: 一意のメタデータフィールド値を取得します。
solution: Experience Manager
title: getUniqueMetadataValues
feature: Dynamic Media Classic,SDK/API，メタデータ
role: Developer,Admin
exl-id: ac5f5667-6c94-425c-bc01-f9df48d16e00
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 25%

---

# getUniqueMetadataValues{#getuniquemetadatavalues}

一意のメタデータフィールド値を取得します。

構文

## 許可されたユーザーの種類 {#section-6a6b67e10a4c4e7bb18306115713380e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-b9d1413811c24566b6d095701f0f66db}

**入力(getUniqueMetadataValuesParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社に取り扱う。 |
| `*`fieldHandle`*` | `xsd:string` | いいえ | メタデータフィールドに対する処理。 |

**出力(getUniqueMetadataValuesReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`値`*` | `type:StringArray` |  |  |

## 例 {#section-440f3bc3e5be436cb6ec26117d05f476}

このコードサンプルでは、フィールドハンドルを使用して特定のメタデータ値を返します。

**リクエスト**

```java
<ns1:getUniqueMetadataValuesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
</ns1:getUniqueMetadataValuesParam>
```

**応答**

```java
<getUniqueMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <values>
      <items>320</items>
   </values>
</getUniqueMetadataValuesReturn>
```
