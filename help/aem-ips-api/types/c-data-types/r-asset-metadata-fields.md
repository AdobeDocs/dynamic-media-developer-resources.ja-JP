---
description: 指定されたアセットタイプのメタデータフィールド定義を返します。
seo-description: 指定されたアセットタイプのメタデータフィールド定義を返します。
seo-title: AssetMetadataFields
solution: Experience Manager
title: AssetMetadataFields
topic: Dynamic Media Image Production System API
uuid: aefb734c-7609-4227-ae2c-48a1469740ec
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---


# AssetMetadataFields{#assetmetadatafields}

指定されたアセットタイプのメタデータフィールド定義を返します。

構文

## パラメータ {#section-5ad771540c5f40c187b35e34aac19305}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`assetType`*` | `xsd:string` | フィールド定義に関連付けられているアセットタイプ（値については、「アセットタイプ」を参照）。 |
| `*`fieldArray`*` | `types:MetadataFieldArray` | `assetType`で指定されたアセットタイプに関連付けられたメタデータフィールド定義の配列。 |

