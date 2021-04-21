---
description: Linuxに画像サービングをインストールした後、インストールを確認します。
solution: Experience Manager
title: インストールの確認
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '137'
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

応答で、「`imageServer.`」で始まる項目が存在するかどうかを確認します。これは、プラットフォームサーバーがImage Serverと正常に通信できたことを示します。
>ドキュメントおよびDemoパッケージのサンプルページを使用して、追加の検証を行うことができます（インストールされている場合）。

