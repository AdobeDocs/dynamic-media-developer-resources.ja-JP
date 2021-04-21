---
description: アセットセットを更新します。
solution: Experience Manager
title: updateAssetSet
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 19%

---


# updateAssetSet{#updateassetset}

アセットセットを更新します。

構文

## パラメータ {#section-d7080ccd97334c94860eb107a3e132b2}

**入力(updateAssetSetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 変更する会社セットが含まれる画像へのハンドル。 |
| `*`assetHandle`*` | `xsd:string` | はい | 変更する画像セットのハンドル。 |
| `*`setDefinition`*` | `xsd:string` | いいえ | 画像セットのメンバをリセットします。 |
| `*`thumbAssetHandle`*` | `xsd:string` | いいえ | 画像セットのサムネールとして機能するアセットのハンドル。 |

**出力(updateAssetSetReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
|  |  |  |  |

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

