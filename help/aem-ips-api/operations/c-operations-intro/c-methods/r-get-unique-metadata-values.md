---
description: 一意のメタデータフィールド値を取得します。
solution: Experience Manager
title: getUniqueMetadataValues
feature: Dynamic Mediaクラシック，SDK/API，メタデータ
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 24%

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

