---
description: 指定した画像のPhotoshopパス名の配列を返します。
seo-description: 指定した画像のPhotoshopパス名の配列を返します。
seo-title: getPhotoshopPathNames
solution: Experience Manager
title: getPhotoshopPathNames
topic: Scene7 Image Production System API
uuid: d3f1dea5-393b-498e-963d-37a4e38068a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getPhotoshopPathNames{#getphotoshoppathnames}

指定した画像のPhotoshopパス名の配列を返します。

構文

## 認証されたユーザータイプ {#section-baa0fd4b92bc4ad89809efd659b3a629}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-605a4aab23104489a21f7f7f5849801b}

**入力(getPhotoshopPathNamesParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 操作する画像を含む会社に対する処理。 |
| ` *`assetHandle`*` | `xsd:string` | はい | 画像アセットのハンドル。 |

**出力(getPhotoshopPathNamesReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`pathNameArray`*` | `types:StringArray` | はい | 画像内のPhotoshopパス名の配列です。 |

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

