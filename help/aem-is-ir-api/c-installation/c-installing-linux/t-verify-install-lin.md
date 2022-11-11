---
title: インストールの確認
description: Linux®に画像サービングをインストールした後、インストールを確認します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# インストールの確認{#verifying-the-installation}

Linux®に画像サービングをインストールした後、インストールを確認します。

Image Server は、Linux®デーモンとしてインストールされます。

**インストールを検証するには**

1. 画像サービングが自動的に起動するように設定され、実行中であることを確認します。

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >これらのスクリプトを実行するには、ルート権限が必要です。

1. 同じホストまたは別のホストでインターネットブラウザーを開き、次の既定のサーバー応答を確認します。

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL  http:// *[!DNL server:port]*/ir/render]

応答内で、次で始まる項目が存在するかどうかを確認します： `imageServer`は、 [!DNL Platform Server] は Image Server と正常に通信できませんでした。

>追加の検証は、ドキュメントパッケージとデモパッケージのサンプルページ（インストールされている場合）を使用して実行できます。
