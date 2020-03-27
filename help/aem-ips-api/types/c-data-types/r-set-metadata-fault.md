---
description: batchSetAssetMetadata操作での更新に関する警告またはエラーの詳細。
seo-description: batchSetAssetMetadata操作での更新に関する警告またはエラーの詳細。
seo-title: SetMetadataFault
solution: Experience Manager
title: SetMetadataFault
topic: Scene7 Image Production System API
uuid: 22302bb0-914a-4d50-a188-9c3ee58e0481
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SetMetadataFault{#setmetadatafault}

batchSetAssetMetadata操作での更新に関する警告またはエラーの詳細。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | メタデータが正常に設定されなかったアセット。 |
| ` *`fieldHandle`*` | `xsd:string` | 値が正常に設定されなかったメタデータフィールドのハンドル。 |
| ` *`コード`*` | `xsd:int` | 障害コード。 |
| ` *`理由`*` | `xsd:string` | 障害の説明（プレーンテキスト）。 |

