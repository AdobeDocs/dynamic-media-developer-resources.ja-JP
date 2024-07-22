---
title: AssetMetadataFields
description: 指定されたアセットタイプのメタデータフィールド定義を返します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 8%

---

# [!DNL AssetMetadataFields]{#assetmetadatafields}

指定されたアセットタイプのメタデータフィールド定義を返します。

構文

## パラメーター {#section-5ad771540c5f40c187b35e34aac19305}

| 名前 | 種類 | 説明 |
|---|---|---|
| assetType | `xsd:string` | フィールド定義に関連付けられたアセットタイプ（値については、「アセットタイプ」を参照してください）。 |
| fieldArray | `types:MetadataFieldArray` | `assetType` で指定されたアセットタイプに関連付けられたメタデータフィールド定義の配列。 |
