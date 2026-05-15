---
description: 画像セットを更新します。
solution: Experience Manager
title: updateImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: d8d5fb80-17f1-424f-8a61-27189f87d603
TQID: 'https://experienceleague.adobe.com/b4eYUJJMox5hAC-vQAtOh189M1bP25VcDchnlvAYoHA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 16%

---

# updateImageSet{#updateimageset}

画像セットを更新します。

構文

## パラメーター {#section-3be47dbbce474ce78676b05e163492e3}

**入力（updateImageSetParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 変更する画像セットを含む会社へのハンドル。 |
| assetHandle | `xsd:string` | Ys | 変更する画像セットへのハンドル。 |
| memberArray | `types:ImageSetMemberUpdateArray` | いいえ | 画像セットメンバーをリセットします。 |
| thumbAssetHandle | `xsd:string` | いいえ | 画像セットのサムネールとして機能するアセットのハンドル。 |

**出力（updateImageSetReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| シーケンス |  |  |  |

## 例 {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**リクエスト**

```java
<updateImageSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|381</assetHandle> 
  <memberArray> 
    <items> 
      <assetHandle>a|374</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|375</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|376</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
  </memberArray> 
  <thumbAssetHandle>a|376</thumbAssetHandle> 
</updateImageSetParam>
```

**応答**

```java
<updateImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```
