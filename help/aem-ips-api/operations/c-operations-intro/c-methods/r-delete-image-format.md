---
description: 画像形式を削除します。 saveImageFormatから画像形式ハンドルを取得します。
seo-description: 画像形式を削除します。 saveImageFormatから画像形式ハンドルを取得します。
seo-title: deleteImageFormat
solution: Experience Manager
title: deleteImageFormat
topic: Scene7 Image Production System API
uuid: 70dddde9-830b-4267-8ef5-df5241f549e3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 10%

---


# deleteImageFormat{#deleteimageformat}

画像形式を削除します。 saveImageFormatから画像形式ハンドルを取得します。

構文

## 認証済みユーザータイプ{#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-462c05d9aad746ee8d2be0656041b693}

**入力(deleteImageFormatParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 削除する画像形式が含まれる会社へのハンドルです。 |
| ` *`imageFormatHandle`*` | `xsd:string` | はい | 削除する画像形式のハンドル。 |

**出力(deleteImageFormatParam)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

このコードサンプルを使用すると、会社から画像形式を削除できます。 別の操作から画像形式ハンドルを取得します。

**リクエスト**

```java
<deleteImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageFormatHandle>47|301</imageFormatHandle>
</deleteImageFormatParam>
```

**応答**

なし

**関連トピック：**

[saveImageFormat](../../../operations/c-operations-intro/c-methods/r-save-image-format.md#reference-d15c27f533ef41e38b54a539a304bd1d)
