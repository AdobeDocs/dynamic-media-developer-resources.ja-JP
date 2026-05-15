---
description: アセットを削除します。
solution: Experience Manager
title: deleteAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dacea36e-3d40-4aaf-94fd-f0709830caf9
TQID: 'https://experienceleague.adobe.com/aZnVNkDpTGXy7OrqVts-KHyOB-gdsA8XYlICQ-JC6aM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 92
ht-degree: 9%

---

# deleteAsset{#deleteasset}

アセットを削除します。

構文

## 承認済みユーザータイプ {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーには、アセットへの読み取りおよび削除アクセス権が必要です。

## パラメーター {#section-0eed164e278b456fbdfb7a50727a0416}

**入力（deleteAssetParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | フォルダーが属する会社へのハンドル。 |
| assetHandle | `xsd:string` | はい | 削除するアセットへのハンドル。 |

**出力（deleteAssetParam）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-d5657289f5234bb0a613dcf691507958}

このサンプルコードは、特定の会社から任意のタイプのアセットを削除します。 アセットハンドルが必要です。別の操作から取得する必要があります。

**リクエスト**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**応答**

なし
