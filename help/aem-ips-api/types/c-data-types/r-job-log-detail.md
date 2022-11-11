---
description: ジョブのログ情報。
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 8%

---

# [!DNL JobLogDetail]{#joblogdetail}

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
