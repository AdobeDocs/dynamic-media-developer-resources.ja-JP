---
description: Linuxでの画像サービングの開始と停止には2つの方法があります。
solution: Experience Manager
title: Linuxでの起動と停止
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---


# Linuxでの起動と停止{#starting-or-stopping-on-linux}

Linuxでの画像サービングの開始と停止には2つの方法があります。

* 開始、停止、検証を行うスクリプトは、画像サービングの[!DNL ImageServing/bin]フォルダーにあります。

   `ImageServing.sh {start|stop|restart|status}`
* 次の代替方法は、システム管理者にとって理解している必要があります。

   `/sbin/service ImageServing {start|stop|status}`
