---
description: batchSetAssetMetadata操作の歌の更新に関する警告またはエラーの詳細です。
seo-description: batchSetAssetMetadata操作の歌の更新に関する警告またはエラーの詳細です。
seo-title: SetMetadataFault
solution: Experience Manager
title: SetMetadataFault
topic: Scene7 Image Production System API
uuid: 22302bb0-914a-4d50-a188-9c3ee58e0481
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 9%

---


# SetMetadataFault{#setmetadatafault}

batchSetAssetMetadata操作の歌の更新に関する警告またはエラーの詳細です。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | メタデータが正常に設定されなかったアセットです。 |
| ` *`fieldHandle`*` | `xsd:string` | 値が正常に設定されなかったメタデータフィールドへのハンドルです。 |
| ` *`コード`*` | `xsd:int` | エラーコード。 |
| ` *`理由`*` | `xsd:string` | フォルトの説明（プレーンテキスト）。 |

