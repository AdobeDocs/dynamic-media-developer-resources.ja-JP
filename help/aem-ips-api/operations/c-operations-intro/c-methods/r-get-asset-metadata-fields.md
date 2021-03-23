---
description: アセットタイプ別にグループ化された、すべてのメタデータフィールドを返します。
seo-description: アセットタイプ別にグループ化された、すべてのメタデータフィールドを返します。
seo-title: getAssetMetadataFields
solution: Experience Manager
title: getAssetMetadataFields
uuid: 01d5076f-f187-4069-b2f2-806fb1d8be84
feature: Dynamic Mediaクラシック，SDK/API，メタデータ，アセット管理
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 18%

---


# getAssetMetadataFields{#getassetmetadatafields}

アセットタイプ別にグループ化された、すべてのメタデータフィールドを返します。

構文

## 認証済みユーザータイプ{#section-e19a9d21cc2b45469c233d4ae55ebfc2}

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

