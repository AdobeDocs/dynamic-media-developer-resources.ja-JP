---
description: Zipファイルのデータを返します。
solution: Experience Manager
title: getZipEntries
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 20%

---


# getZipEntries{#getzipentries}

Zipファイルのデータを返します。

構文

## 認証済みユーザータイプ{#section-33a3f03ba8a14086922397619ce12ab8}

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
| `*`assetHandle`*` | `xsd:string` | はい | ZIPファイルへのハンドル。 |

**出力(getZipEntriesReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`zipArray`*` | `types:ZipEntryArray` | はい | Zipファイル内のエントリの配列。 |

## 例 {#section-1fc0ad8fa448492cb5a135d3e3d161ac}

このコードのサンプルを使用すると、圧縮サイズと非圧縮サイズを含むZipファイル情報を返すことができます。

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

