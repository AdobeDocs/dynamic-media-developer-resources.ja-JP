---
title: インストールの確認
description: Dynamic Media Image Serving をインストールした後、インストールを確認する必要があります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# インストールの確認 {#verifying-the-installation}

Dynamic Media Image Serving をインストールした後、インストールを確認する必要があります。

Image Server は Windows サービスとしてインストールされています。

1. サービスCampaign コントロールパネルを開き、 `Dynamic Media Image Serving` が `Started`.
1. 同じホストまたは別のホストでインターネットブラウザーを開き、次の既定のサーバー応答を確認します。

   `http:// server:port /is/image`

[!DNL  http:// *[!DNL server:port]*/ir/render]

「 `imageServer.`」項目が含まれます。これは、Image Server がリッスンしていることを示します。
>追加の検証は、ドキュメントパッケージとデモパッケージのサンプルページ（インストールされている場合）を使用して実行できます。
