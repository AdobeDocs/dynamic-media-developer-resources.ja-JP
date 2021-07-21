---
description: Zipファイルデータを返します。
solution: Experience Manager
title: getZipEntries
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: eb052685-b750-4a12-b00e-28e676340e98
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 21%

---

# getZipEntries{#getzipentries}

Zipファイルデータを返します。

構文

## 許可されたユーザーの種類 {#section-33a3f03ba8a14086922397619ce12ab8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-aa3f498fe76d4a5f99c42d64520fadce}

**入力(getZipEntriesParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | Zipファイルを含む会社へのハンドル。 |
| `*`assetHandle`*` | `xsd:string` | はい | ZIPファイルを処理します。 |

**出力(getZipEntriesReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`zipArray`*` | `types:ZipEntryArray` | はい | Zipファイル内のエントリの配列。 |

## 例 {#section-1fc0ad8fa448492cb5a135d3e3d161ac}

このコードサンプルは、圧縮サイズと非圧縮サイズを含むZipファイル情報を返します。

**リクエスト**

```java
<getZipEntriesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|94223|27|30602</assetHandle>
</getZipEntriesParam>
```

**応答**

```java
<getZipEntriesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zipArray
      <items>
         <name>Checklist_Images/.DS_Store</name>
         <isDirectory>false</isDirectory>
         <lastModified>2007-05-09T15:41:52.000-07:00</lastModified>
         <compressedSize>503</compressedSize>
         <uncompressedSize>6148</uncompressedSize>
      </items>
   ...
   </zipArray>
</getZipEntriesReturn>
```
