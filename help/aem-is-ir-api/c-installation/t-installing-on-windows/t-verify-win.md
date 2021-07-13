---
description: Dynamic Media Image Servingをインストールした後、インストールを確認する必要があります。
solution: Experience Manager
title: インストールの確認
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# インストールの確認{#verifying-the-installation}

Dynamic Media Image Servingをインストールした後、インストールを確認する必要があります。

Image ServerはWindowsサービスとしてインストールされます。

1. サービスCampaign コントロールパネルを開き、「Dynamic Media画像サービング」のステータスが「開始済み」であることを確認します。
1. 同じホストまたは別のホストでインターネットブラウザーを開き、次の既定のサーバー応答を確認します。

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

応答に「 `imageServer.` 」項目が存在するかどうかを確認します。これは、Image Serverがリッスンしていることを示します。
>追加の検証は、ドキュメントパッケージとデモパッケージのサンプルページ（インストールされている場合）を使用して実行できます。
