---
title: インストールの確認
description: Linux® で画像サービングをインストールしたら、インストールを確認します。
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

Linux® で画像サービングをインストールしたら、インストールを確認します。

Image Server は Linux® デーモンとしてインストールされます。

**インストールを確認するには**

1. 画像サービングが自動的に開始するように設定され、実行中であることを確認します。

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >これらのスクリプトを実行するには、root 権限が必要です。

1. 同じホストまたは別のホストでインターネット ブラウザを開き、既定のサーバー応答を確認します。

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL &#x200B; http:// *[!DNL server:port]*/ir/render]

応答で、`imageServer` で始まる項目が存在するかどうかを確認します。これは、[!DNL Platform Server] が Image Server と正常に通信できることを示しています。

>インストールされている場合は、ドキュメントパッケージとデモパッケージのサンプルページを使用して、追加の検証を実行できます。
