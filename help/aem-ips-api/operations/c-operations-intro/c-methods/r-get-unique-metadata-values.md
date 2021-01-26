---
description: 一意のメタデータフィールド値を取得します。
seo-description: 一意のメタデータフィールド値を取得します。
seo-title: getUniqueMetadataValues
solution: Experience Manager
title: getUniqueMetadataValues
topic: Dynamic Media Image Production System API
uuid: 5b2f95a7-cc0b-4938-99b9-2aefa0ffe693
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 25%

---


# getUniqueMetadataValues{#getuniquemetadatavalues}

一意のメタデータフィールド値を取得します。

構文

## 認証済みユーザータイプ{#section-6a6b67e10a4c4e7bb18306115713380e}

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
| `*`companyHandle`*` | `xsd:string` | はい | 会社へのハンドル。 |
| `*`fieldHandle`*` | `xsd:string` | いいえ | メタデータフィールドへのハンドル。 |

**出力(getUniqueMetadataValuesReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`値`*` | `type:StringArray` |  |  |

## 例 {#section-440f3bc3e5be436cb6ec26117d05f476}

このコードのサンプルでは、フィールドハンドルを使用して特定のメタデータ値を返します。

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

