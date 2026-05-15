---
description: アセットセットを更新します。
solution: Experience Manager
title: updateAssetSet
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: af7899c4-a95f-42c8-858e-ed1592c6f5b6
TQID: 'https://experienceleague.adobe.com/D74n9esGrb36fQcp35KsbB2DNEuddDt4EaKTH4uLlek'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 77
ht-degree: 18%

---

# updateAssetSet{#updateassetset}

アセットセットを更新します。

構文

## パラメーター {#section-d7080ccd97334c94860eb107a3e132b2}

**入力（updateAssetSetParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 変更する画像セットを含む会社へのハンドル。 |
| assetHandle | `xsd:string` | はい | 変更する画像セットへのハンドル。 |
| setDefinition | `xsd:string` | いいえ | 画像セットメンバーをリセットします。 |
| thumbAssetHandle | `xsd:string` | いいえ | 画像セットのサムネールとして機能するアセットのハンドル。 |

**出力（updateAssetSetReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
|   |  |  |  |

## 例 {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**リクエスト**

```java
<updateAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|535</assetHandle> 
  <setDefinition>${getCatalogId([a|202])};${getCatalogId([a|202])};advanced_image;,${getCatalogId([a|935])};${getCatalogId([a|935])};advanced_image;,${getCatalogId([a|933])};${getCatalogId([a|933])};advanced_image;</setDefinition> 
  <thumbAssetHandle>a|202</thumbAssetHandle> 
</updateAssetSetParam>
```

**応答**

```java
<updateAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```
