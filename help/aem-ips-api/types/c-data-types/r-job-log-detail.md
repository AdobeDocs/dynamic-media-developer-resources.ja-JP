---
description: ジョブログ情報。
seo-description: ジョブログ情報。
seo-title: JobLogDetail
solution: Experience Manager
title: JobLogDetail
topic: Scene7 Image Production System API
uuid: cb1879d7-a554-4ff0-bba0-0758c43f2a99
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 7%

---


# JobLogDetail{#joblogdetail}

ジョブログ情報。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`logMessage`*` | `xsd:string` | ジョブログ内のメッセージ。 |
| ` *`logType`*` | `xsd:string` | ジョブログファイルの種類。 |
| ` *`assetName`*` | `xsd:string` | ジョブログ内のアセットの名前（オプション）。 |
| ` *`assetType`*` | `xsd:string` | アセットタイプの選択 |
| ` *`assetHandle`*` | `xsd:string` | ジョブログで参照されているアセットハンドル。 |
| ` *`auxArray`*` | `types:JobLogDetailAuxArray` | 上記の5種類のジョブログの他に、追加の詳細なジョブログ情報を提供します。 |

