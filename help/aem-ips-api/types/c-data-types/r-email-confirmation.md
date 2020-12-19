---
description: cdnCacheInvalidation操作に応答して、指定した受信者に電子メールを送信します。
seo-description: cdnCacheInvalidation操作に応答して、指定した受信者に電子メールを送信します。
seo-title: EmailConfirmation
solution: Experience Manager
title: EmailConfirmation
topic: Scene7 Image Production System API
uuid: c3b7aada-a03a-418d-80b2-31a86a1af786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 5%

---


# EmailConfirmation{#emailconfirmation}

cdnCacheInvalidation操作に応答して、指定した受信者に電子メールを送信します。

構文

## パラメータ {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`ccOriginator`*` | `xsd:boolean` | trueの場合は、ユーザーのWebサービスユーザーアカウントが含まれます。このアカウントは、Scene7CDNから電子メール確認を受け取るように指定された電子メールのリストです。 |
| ` *`ccOthersArray`*` | `types:EmailArray` | Scene7CDNから確認通知を受信するように指定された電子メールアドレス（最大5個）の配列。 |

