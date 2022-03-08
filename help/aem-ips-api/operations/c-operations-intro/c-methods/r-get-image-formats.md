---
description: 画像形式 (PDF、EPS、SWFなど ) を返します。
solution: Experience Manager
title: getImageFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c2fa4cdd-fb4f-4e6a-8197-8f64c986c3a0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 20%

---

# getImageFormats{#getimageformats}

画像形式 (PDF、EPS、SWFなど ) を返します。

構文

## 認証済みユーザータイプ {#section-6a386ad8641b4aa1a281600fc94fd3f6}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-eefa36a70b74498f8727ef61d98cfb63}

**入力 (getImageFormatsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 取得する画像形式を持つ会社へのハンドル。 |

**出力 (getImageFormatsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| imageFormatArray | `types:ImageFormatArray` | はい | 画像形式の配列。 |

## 例 {#section-73881e12839b4904bf3299b0920bdd0c}

このコードサンプルは、指定した会社のすべての画像形式を返します。

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
