---
description: Scene7画像サービングをインストールした後、インストールを検証する必要があります。
seo-description: Scene7画像サービングをインストールした後、インストールを検証する必要があります。
seo-title: インストールの確認
solution: Experience Manager
title: インストールの確認
topic: Scene7 Image Serving - Image Rendering API
uuid: ccc7688d-3d7f-4066-a19e-8a36ca56d711
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# インストールの確認{#verifying-the-installation}

Scene7画像サービングをインストールした後、インストールを検証する必要があります。

Image ServerはWindowsサービスとしてインストールされます。

1. サービスCampaign コントロールパネルを開き、「Scene7画像サービング」のステータスが「開始」であることを確認します。
1. 同じホストまたは別のホストでインターネットブラウザーを開き、既定のサーバー応答を確認します。

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

応答内に「`imageServer.`」項目が存在するかどうかを確認します。これは、Image Serverがリスンしていることを示します。
>ドキュメントおよびDemoパッケージのサンプルページを使用して、追加の検証を行うことができます（インストールされている場合）。

