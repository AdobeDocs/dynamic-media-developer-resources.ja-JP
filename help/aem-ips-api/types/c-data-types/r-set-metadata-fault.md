---
description: batchSetAssetMetadata操作のセグメント更新に関する警告またはエラーの詳細。
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API，メタデータ
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 10%

---

# SetMetadataFault{#setmetadatafault}

batchSetAssetMetadata操作のセグメント更新に関する警告またはエラーの詳細。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | メタデータが正常に設定されなかったアセット。 |
| `*`fieldHandle`*` | `xsd:string` | 値が正常に設定されなかったメタデータフィールドへのハンドル。 |
| `*`コード`*` | `xsd:int` | 障害コード。 |
| `*`理由`*` | `xsd:string` | フォルトの説明（プレーンテキスト）。 |
