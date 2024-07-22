---
description: 指定された画像のPhotoshop パス名の配列を返します。
solution: Experience Manager
title: getPhotoshopPathNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 11d4c0d0-a3a3-4324-a4a6-1dd7b7e673da
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 16%

---

# getPhotoshopPathNames{#getphotoshoppathnames}

指定された画像のPhotoshop パス名の配列を返します。

構文

## 許可されているユーザータイプ {#section-baa0fd4b92bc4ad89809efd659b3a629}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-605a4aab23104489a21f7f7f5849801b}

**入力（getPhotoshopPathNamesParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 使用する画像を含む会社をハンドルします。 |
| assetHandle | `xsd:string` | はい | 画像アセットへのハンドル。 |

**出力（getPhotoshopPathNamesReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| pathNameArray | `types:StringArray` | はい | 画像内のPhotoshop パス名の配列。 |

## 例 {#section-6d316f14b4184d42af4ca3f717b042dd}

**リクエスト**

```java
<getPhotoshopPathNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
</getPhotoshopPathNamesParam>
```

**応答**

```java
<getPhotoshopPathNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <pathNameArray>
    <items>Background Path</items>
    <items>Face Path</items>
  </pathNameArray>
</getPhotoshopPathNamesReturn>
```
