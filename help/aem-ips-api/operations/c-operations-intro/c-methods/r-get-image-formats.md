---
description: PDF、EPS、SWFなどの画像形式を返します。
seo-description: PDF、EPS、SWFなどの画像形式を返します。
seo-title: getImageFormats
solution: Experience Manager
title: getImageFormats
topic: Scene7 Image Production System API
uuid: 0adf989d-9c72-4337-99c0-de6931943e78
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getImageFormats{#getimageformats}

PDF、EPS、SWFなどの画像形式を返します。

構文

## 認証されたユーザータイプ {#section-6a386ad8641b4aa1a281600fc94fd3f6}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-eefa36a70b74498f8727ef61d98cfb63}

**Input (getImageFormatsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 取得する画像形式を持つ会社のハンドル。 |

**出力(getImageFormatsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`imageFormatArray`*` | `types:ImageFormatArray` | はい | 画像形式の配列。 |

## 例 {#section-73881e12839b4904bf3299b0920bdd0c}

このコードサンプルを使用すると、指定した会社のすべての画像形式を返すことができます。

**リクエスト**

```java
<ns1:getImageFormatsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getImageFormatsParam>
```

**応答**

```java
<getImageFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <imageFormatArray></imageFormatArray>
</getImageFormatsReturn>
```

