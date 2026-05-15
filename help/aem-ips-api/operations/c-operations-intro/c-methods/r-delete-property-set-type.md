---
description: プロパティセットタイプとそれに関連するプロパティセットおよびプロパティを削除します。
solution: Experience Manager
title: deletePropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 97ec0f41-794f-4340-b86d-ab07a742d447
TQID: 'https://experienceleague.adobe.com/MslFY4FLpUm0zZRKTL6ZK4-seRyEMbF55r1LRToIFQY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 93
ht-degree: 8%

---

# deletePropertySetType{#deletepropertysettype}

プロパティセットタイプとそれに関連するプロパティセットおよびプロパティを削除します。

構文

## 承認済みユーザータイプ {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-1c8973f5d35f44b4a6a483a41609e455}

**入力（deletePropertySetTypeParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| typeHandle | `xsd:string` | はい | 削除するプロパティセットタイプのハンドル。 |

**出力（deletePropertySetTypeParam）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-85faa2e3411a4e23aa6489037f7ce078}

このコード サンプルでは、プロパティ セット タイプを削除するために、IPS Web サービス サーバーに送信された`deletePropertySetTypeParam`のフィールドとして、タイプのハンドルを使用しています。

**リクエスト**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**応答**

なし
