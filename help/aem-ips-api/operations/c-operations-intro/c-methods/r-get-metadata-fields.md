---
description: アセットに関連付けられたユーザー定義のメタデータフィールドを取得します。
solution: Experience Manager
title: getMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 4d01e2e7-9b68-4dfa-9fe8-08a22cb4bfd5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 12%

---

# getMetadataFields{#getmetadatafields}

アセットに関連付けられたユーザー定義のメタデータフィールドを取得します。

構文

## 許可されているユーザータイプ {#section-e32e481a02674b729bfc5454a6c9ff65}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-bac949e59c0546429c5786fe422d750d}

**入力（getMetadataFieldsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社のハンドル。 |
| assetType | `xsd:string` | はい | メタデータの取得元となるアセットタイプ。 |

**出力（getMetadataFieldsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| コードフレーズ | `Code Phrase` |  |  |

## 例 {#section-dbfde1483d614b5aac2b491cb32115d7}

このコードサンプルでは、指定したタイプおよび会社のメタデータアセットを返します。 応答には、メタデータフィールドの配列がフィールド配列に含まれています。 すべてのアセットに同じメタデータがあるわけではありません。 IPS ユーザーは、アセットのメタデータフィールドを定義します。

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
