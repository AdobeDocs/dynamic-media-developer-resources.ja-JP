---
description: 画像形式を削除します。 saveImageFormatから画像形式ハンドルを取得します。
solution: Experience Manager
title: deleteImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bd717c08-6da4-47f1-8614-e4ba79d8176c
TQID: 'https://experienceleague.adobe.com/BOhXqXdUG6BUA9VsI9faDIeRfdCwlqYsj6sqS-uQ330'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 102
ht-degree: 8%

---

# deleteImageFormat{#deleteimageformat}

画像形式を削除します。 saveImageFormatから画像形式ハンドルを取得します。

構文

## 承認済みユーザータイプ {#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-462c05d9aad746ee8d2be0656041b693}

**入力（deleteImageFormatParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 削除する画像形式を含む会社へのハンドル。 |
| imageFormatHandle | `xsd:string` | はい | 削除する画像形式へのハンドル。 |

**出力（deleteImageFormatParam）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

このコードサンプルは、企業から画像形式を削除します。 別の操作から画像形式のハンドルを取得します。

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
