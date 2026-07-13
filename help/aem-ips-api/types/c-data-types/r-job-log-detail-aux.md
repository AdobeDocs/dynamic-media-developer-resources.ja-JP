---
description: メイン ジョブ ログ メッセージ（JobDetail）に関連付けられた補足メッセージが含まれます。 現在処理中のアセットに関連する警告やその他の詳細が含まれます。
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
TQID: 'https://experienceleague.adobe.com/Hl3L69Hd6Hm8acRaPgFVQCfo8PffGCn5fNGxthmStFM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 64
ht-degree: 6%

---

# [!DNL JobLogDetailAux]{#joblogdetailaux}

メイン ジョブ ログ メッセージ（JobDetail）に関連付けられた補足メッセージが含まれます。 現在処理中のアセットに関連する警告やその他の詳細が含まれます。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| logMessage | `xsd:string` | 補助メッセージ。 |
| logType | `xsd:string` | ログの種類：`IPSJobLog.gcUploadWarning`または`IPSJobLog.gcUploadError` |
| dateCreated | `xsd:dateTime` | 補助ジョブログ作成日。 |

