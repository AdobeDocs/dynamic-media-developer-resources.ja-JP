---
description: batchSetAssetMetadata操作の歌の更新に関する警告またはエラーの詳細です。
seo-description: batchSetAssetMetadata操作の歌の更新に関する警告またはエラーの詳細です。
seo-title: SetMetadataFault
solution: Experience Manager
title: SetMetadataFault
uuid: 22302bb0-914a-4d50-a188-9c3ee58e0481
feature: Dynamic Mediaクラシック，SDK/API，メタデータ
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 8%

---


# SetMetadataFault{#setmetadatafault}

batchSetAssetMetadata操作の歌の更新に関する警告またはエラーの詳細です。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | メタデータが正常に設定されなかったアセットです。 |
| `*`fieldHandle`*` | `xsd:string` | 値が正常に設定されなかったメタデータフィールドへのハンドルです。 |
| `*`コード`*` | `xsd:int` | エラーコード。 |
| `*`理由`*` | `xsd:string` | フォルトの説明（プレーンテキスト）。 |

