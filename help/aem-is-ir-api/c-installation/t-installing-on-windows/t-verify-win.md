---
title: インストールの確認
description: Dynamic Media Image Servingをインストールした後、インストールを確認する必要があります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
TQID: 'https://experienceleague.adobe.com/2i1-Ncy7lyIbm8BHFZGVLNIDnZUOA9sr3tZ970WswL4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 0%

---

# インストールの確認 {#verifying-the-installation}

Dynamic Media Image Servingをインストールした後、インストールを確認する必要があります。

Image ServerはWindows サービスとしてインストールされます。

1. サービス Campaign コントロールパネルを開き、`Dynamic Media Image Serving`がステータス `Started`で存在することを確認します。
1. 同じホストまたは別のホストでインターネットブラウザーを開き、デフォルトのサーバー応答を確認します。

   `http:// server:port /is/image`

[!DNL  http:// *[!DNL server:port]*/ir/render]

応答に「`imageServer.`」項目が含まれていることを確認します。これは、Image Serverがリッスンしていることを示します。

>インストールされている場合は、ドキュメントとデモパッケージのサンプルページを使用して、追加の検証を実行できます。

