---
description: ジョブログ情報。
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
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

