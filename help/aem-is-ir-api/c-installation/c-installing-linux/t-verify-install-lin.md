---
description: Linuxに画像サービングをインストールした後、インストールを確認します。
solution: Experience Manager
title: インストールの確認
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# インストールの確認{#verifying-the-installation}

Linuxに画像サービングをインストールした後、インストールを確認します。

Image Serverは、Linuxデーモンとしてインストールされます。

**インストールを検証するには**

1. 画像サービングが自動的に起動するように設定され、実行中であることを確認します。

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >これらのスクリプトを実行するには、root権限が必要です。

1. 同じホストまたは別のホストでインターネットブラウザーを開き、デフォルトのサーバー応答を確認します。

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL http:// *[!DNL server:port]*/ir/render]

応答で、「 `imageServer.` 」で始まる項目が存在することを確認します。これは、Platform ServerがImage Serverと正常に通信できたことを示します。
>追加の検証は、ドキュメントパッケージとデモパッケージのサンプルページ（インストールされている場合）を使用して実行できます。
