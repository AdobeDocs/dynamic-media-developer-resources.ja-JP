---
description: cdnCacheInvalidation操作に応答して、指定した受信者に電子メールを送信します。
solution: Experience Manager
title: EmailConfirmation
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---


# EmailConfirmation{#emailconfirmation}

cdnCacheInvalidation操作に応答して、指定した受信者に電子メールを送信します。

構文

## パラメータ {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | trueの場合は、ユーザーのWebサービスユーザーアカウントが含まれます。このアカウントは、Dynamic MediaCDNから電子メール確認を受け取るように指定された電子メールのリストです。 |
| `*`ccOthersArray`*` | `types:EmailArray` | Dynamic MediaCDNから確認通知を受信するように指定された電子メールアドレス（最大5個）の配列。 |

