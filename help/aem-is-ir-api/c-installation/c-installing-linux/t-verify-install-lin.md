---
description: Linuxに画像サービングをインストールした後、インストールを確認します。
seo-description: Linuxに画像サービングをインストールした後、インストールを確認します。
seo-title: インストールの確認
solution: Experience Manager
title: インストールの確認
topic: Scene7 Image Serving - Image Rendering API
uuid: 4fdf61c7-3c9f-4f3e-9696-60eb7e3f2209
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---


# インストールの確認{#verifying-the-installation}

Linuxに画像サービングをインストールした後、インストールを確認します。

Image Serverは、Linuxデーモンとしてインストールされます。

**インストールを検証するには**

1. 画像サービングが自動的に開始するように設定され、実行されていることを確認します。

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >これらのスクリプトを実行するには、root権限が必要です。

1. 同じホストまたは別のホストでインターネットブラウザを開き、既定のサーバ応答を確認します。

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL http:// *[!DNL server:port]*/ir/render]

応答で、「 `imageServer.`」で始まる項目が存在するかどうかを確認します。これは、PlatformサーバがImage Serverと正常に通信できたことを示します。
>ドキュメントおよびDemoパッケージのサンプルページを使用して、追加の検証を行うことができます（インストールされている場合）。

