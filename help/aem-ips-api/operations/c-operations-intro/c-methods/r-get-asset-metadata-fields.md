---
description: アセットタイプ別にグループ化されたすべてのメタデータフィールドを返します。
seo-description: アセットタイプ別にグループ化されたすべてのメタデータフィールドを返します。
seo-title: getAssetMetadataFields
solution: Experience Manager
title: getAssetMetadataFields
topic: Scene7 Image Production System API
uuid: 01d5076f-f187-4069-b2f2-806fb1d8be84
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getAssetMetadataFields{#getassetmetadatafields}

アセットタイプ別にグループ化されたすべてのメタデータフィールドを返します。

構文

## 認証されたユーザータイプ {#section-e19a9d21cc2b45469c233d4ae55ebfc2}

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
| ` *`companyHandle`*` | `xsd:string` | はい | メタデータを取得する会社のハンドル。 |

**出力(getAssetMetadataFieldsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`assetFieldArray`*` | `types:AssetMetadataFieldsArray` | はい | アセットタイプ別のメタデータフィールドの配列。 |

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
>簡潔にするために切り捨てられました。

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```

