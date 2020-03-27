---
description: Linuxでの画像サービングの起動と停止には、2つのオプションがあります。
seo-description: Linuxでの画像サービングの起動と停止には、2つのオプションがあります。
seo-title: Linuxでの起動と停止
solution: Experience Manager
title: Linuxでの起動と停止
topic: Scene7 Image Serving - Image Rendering API
uuid: 92cf60c4-3f80-42bc-b135-17bc22ba151e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Linuxでの起動と停止{#starting-or-stopping-on-linux}

Linuxでの画像サービングの起動と停止には、2つのオプションがあります。

* 画像サービングの開始、停止および検証のステータスを行うスクリプトは、次のフォルダーにあ [!DNL ImageServing/bin] ります。

   `ImageServing.sh {start|stop|restart|status}`
* 次の方法は、システム管理者にとってよく知られている方法です。

   `/sbin/service ImageServing {start|stop|status}`
