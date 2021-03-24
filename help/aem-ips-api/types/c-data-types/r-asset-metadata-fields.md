---
description: 指定されたアセットタイプのメタデータフィールド定義を返します。
solution: Experience Manager
title: AssetMetadataFields
feature: Dynamic Mediaクラシック，SDK/API，メタデータ，アセット管理
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '58'
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

