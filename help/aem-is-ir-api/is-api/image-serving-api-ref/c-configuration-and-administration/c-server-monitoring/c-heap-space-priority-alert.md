---
description: Javaのガベージコレクションサイクルの直後に、空きJavaヒープ領域が指定したしきい値を下回ると、優先度アラートが送信されます。
solution: Experience Manager
title: ヒープ領域の優先度アラート
feature: Dynamic Media Classic、SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# ヒープ領域の優先度アラート{#heap-space-priority-alert}

Javaのガベージコレクションサイクルの直後に、空きJavaヒープ領域が指定したしきい値を下回ると、優先度アラートが送信されます。

繰り返されるアラートは、Javaヒープ領域を増やすことで対処する必要があります。 その後、`AS::monitorAlertGenerator.heapSpaceResetInterval`で指定された遅延期間が終了するまで、この条件が発生しても電子メールアラートは送信されません。
