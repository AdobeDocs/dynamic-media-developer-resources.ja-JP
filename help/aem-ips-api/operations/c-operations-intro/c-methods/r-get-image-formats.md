---
description: PDF、EPS、SWFなどの画像形式を返します。
solution: Experience Manager
title: getImageFormats
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 18%

---


# getImageFormats{#getimageformats}

PDF、EPS、SWFなどの画像形式を返します。

構文

## 認証済みユーザータイプ{#section-6a386ad8641b4aa1a281600fc94fd3f6}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-eefa36a70b74498f8727ef61d98cfb63}

**入力(getImageFormatsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 取得する会社形式を持つ画像へのハンドル。 |

**出力(getImageFormatsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`imageFormatArray`*` | `types:ImageFormatArray` | はい | 画像形式の配列。 |

## 例 {#section-73881e12839b4904bf3299b0920bdd0c}

次のコードのサンプルを使用すると、指定した会社のすべての画像形式を返すことができます。

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

