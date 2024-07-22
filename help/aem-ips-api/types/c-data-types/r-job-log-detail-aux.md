---
description: メイン・ジョブ・ログ・メッセージ（JobDetail）に関連付けられた補足メッセージが含まれます。 現在処理されているアセットに関連する警告やその他の詳細が含まれます。
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 6%

---

# [!DNL JobLogDetailAux]{#joblogdetailaux}

メイン・ジョブ・ログ・メッセージ（JobDetail）に関連付けられた補足メッセージが含まれます。 現在処理されているアセットに関連する警告やその他の詳細が含まれます。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| logMessage | `xsd:string` | 補助メッセージ。 |
| logType | `xsd:string` | ログタイプ：`IPSJobLog.gcUploadWarning` または `IPSJobLog.gcUploadError`。 |
| dateCreated | `xsd:dateTime` | 補助作業ログ作成日。 |
