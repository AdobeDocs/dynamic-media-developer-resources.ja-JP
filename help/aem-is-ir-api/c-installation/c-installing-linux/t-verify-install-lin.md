---
title: インストールの確認
description: Linux®にImage Servingをインストールしたら、インストールを確認します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
TQID: 'https://experienceleague.adobe.com/LyHlwiFL1b-iwo1kSnUeNfNo3fZY6FZetHgnNFoxGZo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 0%

---

# インストールの確認{#verifying-the-installation}

Linux®にImage Servingをインストールしたら、インストールを確認します。

Image ServerはLinux® デーモンとしてインストールされます。

**インストールを確認するには**

1. 画像サービングが自動的に開始するように設定され、実行されていることを確認します。

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >これらのスクリプトを実行するには、ルート権限が必要です。

1. 同じホストまたは別のホストでインターネットブラウザーを開き、デフォルトのサーバー応答を確認します。

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL &#x200B; http:// *[!DNL server:port]*/ir/render]

応答で、`imageServer`で始まる項目が存在することを確認します。これは、[!DNL Platform Server]がImage Serverと正常に通信できることを示します。

>インストールされている場合は、ドキュメントとデモパッケージのサンプルページを使用して、追加の検証を実行できます。
