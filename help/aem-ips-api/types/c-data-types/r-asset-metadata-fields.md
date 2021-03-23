---
description: 指定されたアセットタイプのメタデータフィールド定義を返します。
seo-description: 指定されたアセットタイプのメタデータフィールド定義を返します。
seo-title: AssetMetadataFields
solution: Experience Manager
title: AssetMetadataFields
uuid: aefb734c-7609-4227-ae2c-48a1469740ec
feature: Dynamic Mediaクラシック，SDK/API，メタデータ，アセット管理
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 7%

---


# AssetMetadataFields{#assetmetadatafields}

指定されたアセットタイプのメタデータフィールド定義を返します。

構文

## パラメータ {#section-5ad771540c5f40c187b35e34aac19305}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`assetType`*` | `xsd:string` | フィールド定義に関連付けられているアセットタイプ（値については、「アセットタイプ」を参照）。 |
| `*`fieldArray`*` | `types:MetadataFieldArray` | `assetType`で指定されたアセットタイプに関連付けられたメタデータフィールド定義の配列。 |

