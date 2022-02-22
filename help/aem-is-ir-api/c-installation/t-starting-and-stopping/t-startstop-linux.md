---
title: Linux®での起動または停止
description: Linux®で画像サービングを起動または停止する方法は 2 つあります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eb4c60b2-5491-40e9-b105-d4b05006a9ca
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# Linux®での起動または停止 {#starting-or-stopping-on-linux}

Linux®で画像サービングを起動または停止する方法は 2 つあります。

* 画像サービングのステータスを検証する、または画像サービングを開始および停止するスクリプトは、 [!DNL ImageServing/bin] フォルダー：

   `ImageServing.sh {start|stop|restart|status}`
* 次の代替手段は、システム管理者にとって理解しておく必要があります。

   `/sbin/service ImageServing {start|stop|status}`
