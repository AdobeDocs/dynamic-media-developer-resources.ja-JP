---
description: アセットタイプ別にグループ化されたすべてのメタデータフィールドを返します。
solution: Experience Manager
title: getAssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 5234d3ea-c333-4e35-91ae-ce3412919fda
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 19%

---

# getAssetMetadataFields{#getassetmetadatafields}

アセットタイプ別にグループ化されたすべてのメタデータフィールドを返します。

構文

## 許可されているユーザータイプ {#section-e19a9d21cc2b45469c233d4ae55ebfc2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-5dd58970d61d4d4a928e36ffceca6f5e}

**入力（getAssetMetadataFieldsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | メタデータを取得する会社へのハンドル。 |

**出力（getAssetMetadataFieldsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| assetFieldArray | `types:AssetMetadataFieldsArray` | はい | アセットタイプごとのメタデータフィールドの配列。 |

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
