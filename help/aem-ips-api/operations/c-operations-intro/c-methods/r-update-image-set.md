---
description: 画像セットを更新します。
solution: Experience Manager
title: updateImageSet
feature: Dynamic Media Classic,SDK/API，画像セット
role: Developer,Administrator
exl-id: d8d5fb80-17f1-424f-8a61-27189f87d603
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 18%

---

# updateImageSet{#updateimageset}

画像セットを更新します。

構文

## パラメータ {#section-3be47dbbce474ce78676b05e163492e3}

**入力(updateImageSetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 変更する画像セットを含む会社へのハンドル。 |
| `*`assetHandle`*` | `xsd:string` | Ys | 変更する画像セットのハンドル。 |
| `*`memberArray`*` | `types:ImageSetMemberUpdateArray` | いいえ | 画像セットのメンバをリセットします。 |
| `*`thumbAssetHandle`*` | `xsd:string` | いいえ | 画像セットのサムネールとして機能するアセットのハンドル。 |

**出力(updateImageSetReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`シーケンス`*` |  |  |  |

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
