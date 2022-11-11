---
description: cdnCacheInvalidation 操作に応じて、指定された受信者に電子メールを送信します。
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 6%

---

# [!DNL EmailConfirmation]{#emailconfirmation}

cdnCacheInvalidation 操作に応じて、指定された受信者に電子メールを送信します。

構文

## パラメータ {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 名前 | 種類 | 説明 |
|---|---|---|
| ccOriginator | `xsd:boolean` | true の場合は、ユーザーの Web サービスユーザーアカウントが含まれます。これは、Dynamic Media CDN から電子メール確認を受け取るように指定された電子メールのリストです。 |
| ccOthersArray | `types:EmailArray` | Dynamic Media CDN から確認通知を受け取るように指定された電子メールアドレス（最大 5 つ）の配列。 |
