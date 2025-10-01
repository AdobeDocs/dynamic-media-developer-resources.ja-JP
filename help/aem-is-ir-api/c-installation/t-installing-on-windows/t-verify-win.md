---
title: インストールの確認
description: Dynamic Media 画像サービングをインストールしたら、インストールを確認します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# インストールの確認 {#verifying-the-installation}

Dynamic Media 画像サービングをインストールしたら、インストールを確認します。

Image Server は Windows サービスとしてインストールされます。

1. サービスCampaign コントロールパネルを開き、`Dynamic Media Image Serving` が `Started` ステータスで存在することを確認します。
1. 同じホストまたは別のホストでインターネット ブラウザを開き、既定のサーバー応答を確認します。

   `http:// server:port /is/image`

[!DNL  http:// *[!DNL server:port]*/ir/render]

応答内に「`imageServer.`」項目があるかどうかを確認します。これは、Image Server がリッスンしていることを示します。

>インストールされている場合は、ドキュメントパッケージとデモパッケージのサンプルページを使用して、追加の検証を実行できます。
