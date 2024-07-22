---
description: 優先度アラートは、Java のガベージコレクションサイクルの直後に、Java の空きヒープ領域が指定されたしきい値を下回ると送信されます。
solution: Experience Manager
title: ヒープ領域優先度アラート
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---

# ヒープ領域優先度アラート{#heap-space-priority-alert}

優先度アラートは、Java のガベージコレクションサイクルの直後に、Java の空きヒープ領域が指定されたしきい値を下回ると送信されます。

アラートを繰り返す場合は、Java のヒープ領域を増やして対処する必要があります。 この条件に続いて発生した場合は、`AS::monitorAlertGenerator.heapSpaceResetInterval` で指定された遅延期間が経過するまで、メールアラートは送信されません。
