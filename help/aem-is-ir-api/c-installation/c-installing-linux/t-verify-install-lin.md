---
description: Linuxに画像サービングをインストールした後、インストールを確認します。
seo-description: Linuxに画像サービングをインストールした後、インストールを確認します。
seo-title: インストールの確認
solution: Experience Manager
title: インストールの確認
topic: Scene7 Image Serving - Image Rendering API
uuid: 4fdf61c7-3c9f-4f3e-9696-60eb7e3f2209
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# インストールの確認{#verifying-the-installation}

Linuxに画像サービングをインストールした後、インストールを確認します。

Image Serverは、Linuxデーモンとしてインストールされます。

**インストールを検証するには**

1. 画像サービングが自動的に開始するように設定され、実行されていることを確認します。

   `> /sbin/service ImageServing status`

   >[!NOTE] {class=&quot;- topic/note &quot;}
   >
   >これらのスクリプトを実行するには、root権限が必要です。

1. 同じホストまたは別のホストでインターネットブラウザーを開き、既定のサーバー応答を確認します。

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL http:// *[!DNL server:port]*/ir/render]

応答内で、「」で始まる項目が存在するかどうかを確認します。これは、プラットフォームサーバ `imageServer.`ーがImage Serverと正常に通信できたことを示します。
>追加の検証は、ドキュメントおよびデモパッケージのサンプルページ（インストールされている場合）を使用して実行できます。

