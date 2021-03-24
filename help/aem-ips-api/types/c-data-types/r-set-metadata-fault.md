---
description: batchSetAssetMetadata操作の歌の更新に関する警告またはエラーの詳細です。
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Mediaクラシック，SDK/API，メタデータ
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 10%

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

