---
description: メインジョブログメッセージ(JobDetail)に関連付けられた補助メッセージが含まれます。 現在処理されているアセットに関連付けられた警告およびその他の詳細が含まれます。
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 6%

---


# JobLogDetailAux{#joblogdetailaux}

メインジョブログメッセージ(JobDetail)に関連付けられた補助メッセージが含まれます。 現在処理されているアセットに関連付けられた警告およびその他の詳細が含まれます。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | 補助メッセージ。 |
| `*`logType`*` | `xsd:string` | ログの種類：`IPSJobLog.gcUploadWarning`または`IPSJobLog.gcUploadError`。 |
| `*`dateCreated`*` | `xsd:dateTime` | 補助的なジョブログ作成日。 |

