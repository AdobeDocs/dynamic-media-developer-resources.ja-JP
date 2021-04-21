---
description: 優先度アラートは、Javaのガベージ収集サイクルの直後に、空きJavaヒープ領域が指定したしきい値を下回った場合に送信されます。
solution: Experience Manager
title: ヒープ領域の優先度の警告
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# ヒープ領域の優先度の警告{#heap-space-priority-alert}

優先度アラートは、Javaのガベージ収集サイクルの直後に、空きJavaヒープ領域が指定したしきい値を下回った場合に送信されます。

Javaヒープ領域を増やすことで、繰り返しアラートに対処する必要があります。 それ以降、`AS::monitorAlertGenerator.heapSpaceResetInterval`で指定された遅延期間が終了するまで、この条件が発生しても電子メールアラートは送信されません。
