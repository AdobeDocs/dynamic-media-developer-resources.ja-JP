---
description: 優先度アラートは、Javaのガベージ収集サイクルの直後に、空きJavaヒープ領域が指定したしきい値を下回った場合に送信されます。
seo-description: 優先度アラートは、Javaのガベージ収集サイクルの直後に、空きJavaヒープ領域が指定したしきい値を下回った場合に送信されます。
seo-title: ヒープ領域の優先度の警告
solution: Experience Manager
title: ヒープ領域の優先度の警告
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# ヒープ領域の優先度の警告{#heap-space-priority-alert}

優先度アラートは、Javaのガベージ収集サイクルの直後に、空きJavaヒープ領域が指定したしきい値を下回った場合に送信されます。

Javaヒープ領域を増やすことで、繰り返しアラートに対処する必要があります。 それ以降、`AS::monitorAlertGenerator.heapSpaceResetInterval`で指定された遅延期間が終了するまで、この条件が発生しても電子メールアラートは送信されません。
