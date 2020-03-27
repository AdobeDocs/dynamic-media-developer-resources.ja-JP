---
description: アセットに関連付けられたユーザ定義のメタデータフィールドを取得します。
seo-description: アセットに関連付けられたユーザ定義のメタデータフィールドを取得します。
seo-title: getMetadataFields
solution: Experience Manager
title: getMetadataFields
topic: Scene7 Image Production System API
uuid: bf891bae-53c8-4e3d-90df-caca9a7e022b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getMetadataFields{#getmetadatafields}

アセットに関連付けられたユーザ定義のメタデータフィールドを取得します。

構文

## 認証されたユーザータイプ {#section-e32e481a02674b729bfc5454a6c9ff65}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-bac949e59c0546429c5786fe422d750d}

**Input (getMetadataFieldsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社が取り扱う。 |
| ` *`assetType`*` | `xsd:string` | はい | メタデータを取得するアセットタイプ。 |

**出力(getMetadataFieldsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`コードフレーズ`*` | `Code Phrase` |  |  |

## 例 {#section-dbfde1483d614b5aac2b491cb32115d7}

このコードサンプルを使用すると、指定したタイプおよび会社のメタデータアセットを返すことができます。 応答には、フィールド配列内のメタデータフィールドの配列が含まれます。 すべてのアセットが同じメタデータを持つわけではありません。 IPSユーザは、アセットのメタデータフィールドを定義します。

**リクエスト**

```java
<ns1:getMetadataFieldsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
</ns1:getMetadataFieldsParam>
```

**応答**

```java
<getMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldArray>
      <items>
         <fieldHandle>47|ALL|Resolution</fieldHandle>
         <name>Resolution</name>
         <type>String</type>
         <defaultValue>120</defaultValue>
         <isRequired>false</isRequired>
         <isUserDefined>true</isUserDefined>
      </items>
   </fieldArray>
</getMetadataFieldsReturn>
```

