---
description: Javaのガベージコレクションサイクルの直後に、空きJavaヒープ領域が指定したしきい値を下回ると、優先度アラートが送信されます。
seo-description: Javaのガベージコレクションサイクルの直後に、空きJavaヒープ領域が指定したしきい値を下回ると、優先度アラートが送信されます。
seo-title: ヒープ領域の優先度のアラート
solution: Experience Manager
title: ヒープ領域の優先度のアラート
topic: Scene7 Image Serving - Image Rendering API
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ヒープ領域の優先度のアラート{#heap-space-priority-alert}

Javaのガベージコレクションサイクルの直後に、空きJavaヒープ領域が指定したしきい値を下回ると、優先度アラートが送信されます。

アラートの繰り返しは、Javaヒープ領域を増やすことで対処する必要があります。 この条件が続けて発生しても、で指定した遅延期間が終了するまで、電子メールアラートは `AS::monitorAlertGenerator.heapSpaceResetInterval` 送信されません。
