---
description: ジョブログ情報。
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---


# JobLogDetail{#joblogdetail}

ジョブログ情報。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | ジョブログ内のメッセージ。 |
| `*`logType`*` | `xsd:string` | ジョブログファイルの種類。 |
| `*`assetName`*` | `xsd:string` | ジョブログ内のアセットの名前（オプション）。 |
| `*`assetType`*` | `xsd:string` | アセットタイプの選択 |
| `*`assetHandle`*` | `xsd:string` | ジョブログで参照されているアセットハンドル。 |
| `*`auxArray`*` | `types:JobLogDetailAuxArray` | 上記の5種類のジョブログの他に、追加の詳細なジョブログ情報を提供します。 |

