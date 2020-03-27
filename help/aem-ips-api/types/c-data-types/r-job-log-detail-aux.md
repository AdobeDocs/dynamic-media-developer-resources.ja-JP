---
description: メインジョブのログメッセージ(JobDetail)に関連付けられた補足メッセージが含まれます。 現在処理されているアセットに関連付けられている警告およびその他の詳細が含まれます。
seo-description: メインジョブのログメッセージ(JobDetail)に関連付けられた補足メッセージが含まれます。 現在処理されているアセットに関連付けられている警告およびその他の詳細が含まれます。
seo-title: JobLogDetailAux
solution: Experience Manager
title: JobLogDetailAux
topic: Scene7 Image Production System API
uuid: df6f61f2-54f1-4996-938c-c3ea8c27551a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# JobLogDetailAux{#joblogdetailaux}

メインジョブのログメッセージ(JobDetail)に関連付けられた補足メッセージが含まれます。 現在処理されているアセットに関連付けられている警告およびその他の詳細が含まれます。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`logMessage`*` | `xsd:string` | 補助メッセージ。 |
| ` *`logType`*` | `xsd:string` | ログの種類：ま `IPSJobLog.gcUploadWarning` た `IPSJobLog.gcUploadError`は |
| ` *`dateCreated`*` | `xsd:dateTime` | 補助的なジョブログの作成日。 |

