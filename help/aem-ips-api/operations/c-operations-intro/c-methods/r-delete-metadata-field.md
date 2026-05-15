---
description: 会社のメタデータフィールドを削除します。
solution: Experience Manager
title: deleteMetadataField
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1922fc1b-2abc-4d31-985a-65c788af4d46
TQID: 'https://experienceleague.adobe.com/GnKkb-vTCdD5PwU111sxefzxR7FN74hk3i66c3gcH9I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 8%

---

# deleteMetadataField{#deletemetadatafield}

会社のメタデータフィールドを削除します。

構文

## 承認済みユーザータイプ {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-73f12a30cc4340b6b32dd11effd5195e}

**入力（deleteMetadataFieldParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 削除するメタデータフィールドを含む会社へのハンドル。 |
| fieldHandle | `xsd:string` | はい | 削除するメタデータフィールドのハンドル。 |

**出力（deleteMetadataFieldParam）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-e1c474ea91a040609ecd7c2400f4fa3c}

このコードサンプルは、会社のメタデータフィールドを削除します。 このアクションを実行するには、IPS Web サービス サーバーに渡される`deleteMetadataFieldParam`のフィールドとして、会社ハンドルとメタデータ ハンドルを使用します。

**リクエスト**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**応答**

なし。0
