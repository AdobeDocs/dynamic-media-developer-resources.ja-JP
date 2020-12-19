---
description: Linuxでの画像サービングの開始と停止には2つの方法があります。
seo-description: Linuxでの画像サービングの開始と停止には2つの方法があります。
seo-title: Linuxでの起動と停止
solution: Experience Manager
title: Linuxでの起動と停止
topic: Scene7 Image Serving - Image Rendering API
uuid: 92cf60c4-3f80-42bc-b135-17bc22ba151e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---


# Linuxでの起動と停止{#starting-or-stopping-on-linux}

Linuxでの画像サービングの開始と停止には2つの方法があります。

* 開始、停止、検証を行うスクリプトは、画像サービングの[!DNL ImageServing/bin]フォルダーにあります。

   `ImageServing.sh {start|stop|restart|status}`
* 次の代替方法は、システム管理者にとって理解している必要があります。

   `/sbin/service ImageServing {start|stop|status}`
