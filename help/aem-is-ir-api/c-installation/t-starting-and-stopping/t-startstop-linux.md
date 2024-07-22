---
title: Linux® での起動または停止
description: Linux® での画像サービングの開始と停止には、2 つのオプションがあります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eb4c60b2-5491-40e9-b105-d4b05006a9ca
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# Linux® での起動または停止 {#starting-or-stopping-on-linux}

Linux® での画像サービングの開始と停止には、2 つのオプションがあります。

* 画像サービングのステータスを確認したり、画像サービングを開始および停止したりするスクリプトは、[!DNL ImageServing/bin] フォルダーにあります。

  `ImageServing.sh {start|stop|restart|status}`
* 次の代替手段は、システム管理者になじみがある必要があります。

  `/sbin/service ImageServing {start|stop|status}`
