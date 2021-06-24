---
description: アセットタイプ別にグループ化された、すべてのメタデータフィールドを返します。
solution: Experience Manager
title: getAssetMetadataFields
feature: Dynamic Media Classic,SDK/API，メタデータ，アセット管理
role: Developer,Administrator
exl-id: 5234d3ea-c333-4e35-91ae-ce3412919fda
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 21%

---

# getAssetMetadataFields{#getassetmetadatafields}

アセットタイプ別にグループ化された、すべてのメタデータフィールドを返します。

構文

## 許可されたユーザーの種類 {#section-e19a9d21cc2b45469c233d4ae55ebfc2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-5dd58970d61d4d4a928e36ffceca6f5e}

**入力(getAssetMetadataFieldsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | メタデータを取得する会社のハンドル。 |

**出力(getAssetMetadataFieldsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`assetFieldArray`*` | `types:AssetMetadataFieldsArray` | はい | アセットタイプ別のメタデータフィールドの配列。 |

## 例 {#section-d79ab85f29144635b0b61416e52f4f3f}

**リクエスト**

```java
<getAssetMetadataFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
</getAssetMetadataFieldsParam>
```

**応答**

>[!NOTE]
>
>簡潔にするために切り捨てられます。

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```
