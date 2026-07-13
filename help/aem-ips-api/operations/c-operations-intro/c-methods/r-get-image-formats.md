---
description: PDF、EPS、SWFなどの画像フォーマットを返します。
solution: Experience Manager
title: getImageFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c2fa4cdd-fb4f-4e6a-8197-8f64c986c3a0
TQID: 'https://experienceleague.adobe.com/L8HQVUaxUxkNNkZU7f9Edmh4-t6iwys4c106YVEczD8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 74
ht-degree: 16%

---

# getImageFormats{#getimageformats}

PDF、EPS、SWFなどの画像フォーマットを返します。

構文

## 承認済みユーザータイプ {#section-6a386ad8641b4aa1a281600fc94fd3f6}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-eefa36a70b74498f8727ef61d98cfb63}

**入力（getImageFormatsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 取得する画像形式を持つ会社へのハンドル。 |

**出力（getImageFormatsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| imageFormatArray | `types:ImageFormatArray` | はい | 画像形式配列。 |

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

