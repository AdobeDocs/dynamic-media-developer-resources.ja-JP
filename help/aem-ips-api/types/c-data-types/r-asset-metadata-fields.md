---
title: AssetMetadataFields
description: 指定したアセットタイプのメタデータフィールド定義を返します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 10%

---

# AssetMetadataFields{#assetmetadatafields}

指定したアセットタイプのメタデータフィールド定義を返します。

構文

## パラメータ {#section-5ad771540c5f40c187b35e34aac19305}

| 名前 | 種類 | 説明 |
|---|---|---|
| assetType | `xsd:string` | フィールド定義に関連付けられたアセットタイプ（値については、「アセットタイプ」を参照）。 |
| fieldArray | `types:MetadataFieldArray` | で指定されたアセットタイプに関連付けられたメタデータフィールド定義の配列 `assetType`. |
