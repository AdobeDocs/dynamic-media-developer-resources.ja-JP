---
description: ジョブ ログ情報。
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 6%

---

# [!DNL JobLogDetail]{#joblogdetail}

ジョブ ログ情報。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| logMessage | `xsd:string` | ジョブ・ログ内のメッセージ。 |
| logType | `xsd:string` | ジョブ ログ ファイルの種類。 |
| assetName | `xsd:string` | ジョブ ログ内のアセットの名前（オプション）。 |
| assetType | `xsd:string` | アセットタイプを選択します。 |
| assetHandle | `xsd:string` | ジョブログで参照されるアセットハンドル。 |
| auxArray | `types:JobLogDetailAuxArray` | 前述の 5 つのジョブ・ログ・タイプ以外にも、詳細なジョブ・ログ情報を提供します。 |
