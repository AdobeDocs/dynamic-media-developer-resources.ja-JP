---
description: メインジョブログメッセージ (JobDetail) に関連付けられた補助メッセージが含まれます。 現在処理されているアセットに関連する警告やその他の詳細が含まれます。
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 7%

---

# [!DNL JobLogDetailAux]{#joblogdetailaux}

メインジョブログメッセージ (JobDetail) に関連付けられた補助メッセージが含まれます。 現在処理されているアセットに関連する警告やその他の詳細が含まれます。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| logMessage | `xsd:string` | 補助メッセージ。 |
| logType | `xsd:string` | ログの種類： `IPSJobLog.gcUploadWarning` または `IPSJobLog.gcUploadError`. |
| dateCreated | `xsd:dateTime` | 補助的なジョブログ作成日。 |
