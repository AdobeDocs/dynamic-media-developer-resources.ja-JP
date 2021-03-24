---
description: Dynamic Media画像サービングをインストールした後、インストールを検証する必要があります。
solution: Experience Manager
title: インストールの確認
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# インストールの確認{#verifying-the-installation}

Dynamic Media画像サービングをインストールした後、インストールを検証する必要があります。

Image ServerはWindowsサービスとしてインストールされます。

1. サービスCampaign コントロールパネルを開き、「Dynamic Media画像サービング」のステータスが「開始」であることを確認します。
1. 同じホストまたは別のホストでインターネットブラウザーを開き、既定のサーバー応答を確認します。

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

応答内に「`imageServer.`」項目が存在するかどうかを確認します。これは、Image Serverがリスンしていることを示します。
>ドキュメントおよびDemoパッケージのサンプルページを使用して、追加の検証を行うことができます（インストールされている場合）。

