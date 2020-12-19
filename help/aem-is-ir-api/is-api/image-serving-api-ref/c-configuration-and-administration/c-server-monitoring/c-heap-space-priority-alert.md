---
description: 優先度アラートは、Javaのガベージ収集サイクルの直後に、空きJavaヒープ領域が指定したしきい値を下回った場合に送信されます。
seo-description: 優先度アラートは、Javaのガベージ収集サイクルの直後に、空きJavaヒープ領域が指定したしきい値を下回った場合に送信されます。
seo-title: ヒープ領域の優先度の警告
solution: Experience Manager
title: ヒープ領域の優先度の警告
topic: Scene7 Image Serving - Image Rendering API
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# ヒープ領域の優先度の警告{#heap-space-priority-alert}

優先度アラートは、Javaのガベージ収集サイクルの直後に、空きJavaヒープ領域が指定したしきい値を下回った場合に送信されます。

Javaヒープ領域を増やすことで、繰り返しアラートに対処する必要があります。 それ以降、`AS::monitorAlertGenerator.heapSpaceResetInterval`で指定された遅延期間が終了するまで、この条件が発生しても電子メールアラートは送信されません。
