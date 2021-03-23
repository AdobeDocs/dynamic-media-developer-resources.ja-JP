---
description: メインジョブログメッセージ(JobDetail)に関連付けられた補助メッセージが含まれます。 現在処理されているアセットに関連付けられた警告およびその他の詳細が含まれます。
seo-description: メインジョブログメッセージ(JobDetail)に関連付けられた補助メッセージが含まれます。 現在処理されているアセットに関連付けられた警告およびその他の詳細が含まれます。
seo-title: JobLogDetailAux
solution: Experience Manager
title: JobLogDetailAux
uuid: df6f61f2-54f1-4996-938c-c3ea8c27551a
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 5%

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

