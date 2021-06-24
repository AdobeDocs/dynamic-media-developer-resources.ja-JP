---
description: 指定されたアセットタイプのメタデータフィールド定義を返します。
solution: Experience Manager
title: AssetMetadataFields
feature: Dynamic Media Classic,SDK/API，メタデータ，アセット管理
role: Developer,Administrator
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '56'
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
