---
description: タスク項目の進捗状況情報。
solution: Experience Manager
title: TaskItemProgress
feature: Dynamic Media Classic、SDK/API
role: Developer,Administrator
exl-id: 568a5601-b928-447d-8297-01139f36cf73
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '38'
ht-degree: 15%

---

# TaskItemProgress{#taskitemprogress}

タスク項目の進捗状況情報。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`itemName`*` | `xsd:string` | 処理中の項目の名前。 |
| `*`progress`*` | `xsd:double` | 進行状況完了%。 |
| `*`progressMessage`*` | `xsd:string` | メッセージを処理します。 |
| `*`lastProgressUpdate`*` | `xsd:dateTime` | 前回の更新時刻。 |
