---
description: Linuxで画像サービングを起動または停止する方法は2つあります。
solution: Experience Manager
title: Linuxでの起動と停止
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: eb4c60b2-5491-40e9-b105-d4b05006a9ca
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# Linuxでの起動と停止{#starting-or-stopping-on-linux}

Linuxで画像サービングを起動または停止する方法は2つあります。

* 画像サービングの開始、停止および検証のステータスを示すスクリプトは、[!DNL ImageServing/bin]フォルダーにあります。

   `ImageServing.sh {start|stop|restart|status}`
* 次の代替手段は、システム管理者にとって理解している必要があります。

   `/sbin/service ImageServing {start|stop|status}`
