---
description: ジョブのログ情報。
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 8%

---

# JobLogDetail{#joblogdetail}

ジョブのログ情報。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| logMessage | `xsd:string` | ジョブログ内のメッセージ。 |
| logType | `xsd:string` | ジョブのログファイルの種類。 |
| assetName | `xsd:string` | ジョブログ内のアセットの名前（オプション）。 |
| assetType | `xsd:string` | アセットタイプの選択。 |
| assetHandle | `xsd:string` | ジョブログで参照されるアセットハンドル。 |
| auxArray | `types:JobLogDetailAuxArray` | 上記の 5 つのジョブログタイプ以外の詳細なジョブログ情報を提供します。 |
