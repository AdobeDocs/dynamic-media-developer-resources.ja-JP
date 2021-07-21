---
description: cdnCacheInvalidation操作に応じて、指定された受信者に電子メールを送信します。
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 6%

---

# EmailConfirmation{#emailconfirmation}

cdnCacheInvalidation操作に応じて、指定された受信者に電子メールを送信します。

構文

## パラメータ {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | trueの場合は、ユーザーのWebサービスユーザーアカウントが含まれます。これは、Dynamic Media CDNから電子メール確認を受け取るように指定された電子メールのリストです。 |
| `*`ccOthersArray`*` | `types:EmailArray` | Dynamic Media CDNから確認通知を受信するように指定された電子メールアドレスの配列（最大5個）。 |
