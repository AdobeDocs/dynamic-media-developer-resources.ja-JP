---
description: cdnCacheInvalidation操作に応答して、指定された受信者に電子メールを送信します。
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
TQID: 'https://experienceleague.adobe.com/h9ZZRR0zR347mzSifomCmtNW5GorTC6fgGjeSRf52KU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 5%

---

# [!DNL EmailConfirmation]{#emailconfirmation}

cdnCacheInvalidation操作に応答して、指定された受信者に電子メールを送信します。

構文

## パラメーター {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 名前 | 種類 | 説明 |
|---|---|---|
| ccOriginator | `xsd:boolean` | trueの場合は、ユーザーのweb サービスユーザーアカウントが含まれます。これは、Dynamic Media CDNからメール確認を受信するように指定されたメールのリストです。 |
| ccOthersArray | `types:EmailArray` | Dynamic Media CDNから確認通知を受け取るように指定されたメールアドレスの配列（最大5つ）。 |

