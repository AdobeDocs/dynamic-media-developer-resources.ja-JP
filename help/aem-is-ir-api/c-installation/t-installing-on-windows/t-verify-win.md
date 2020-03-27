---
description: Scene7画像サービングをインストールした後、インストールを確認する必要があります。
seo-description: Scene7画像サービングをインストールした後、インストールを確認する必要があります。
seo-title: インストールの確認
solution: Experience Manager
title: インストールの確認
topic: Scene7 Image Serving - Image Rendering API
uuid: ccc7688d-3d7f-4066-a19e-8a36ca56d711
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# インストールの確認{#verifying-the-installation}

Scene7画像サービングをインストールした後、インストールを確認する必要があります。

Image Serverは、Windowsサービスとしてインストールされます。

1. サービスコントロールパネルを開き、「Scene7 Image Serving」のステータスが「開始済み」であることを確認します。
1. 同じホストまたは別のホストでインターネットブラウザーを開き、次の既定のサーバー応答を確認します。

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

応答内に「」項目が存在する `imageServer.`かどうかを確認します。これは、Image Serverがリスンしていることを示します。
>追加の検証は、ドキュメントおよびデモパッケージのサンプルページ（インストールされている場合）を使用して実行できます。

