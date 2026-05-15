---
description: これは、 [!DNL Platform Server]に対するすべてのHTTP リクエストを追跡するプライマリログです。 画像レンダリングを有効にすると、アクセスログデータが同じファイルに書き込まれます。
solution: Experience Manager
title: アクセスログ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
TQID: 'https://experienceleague.adobe.com/PXdlJ0gBGbq4FFhoG6gtmG3hrWVWsXIPelL9xXy5ESk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 135
ht-degree: 0%

---

# アクセスログ{#access-log}

これは、[!DNL Platform Server]に対して行われたすべてのHTTP リクエストを追跡するプライマリログです。 画像レンダリングを有効にすると、アクセスログデータが同じファイルに書き込まれます。

アクセスログはserver.xmlで設定されます。

>[!NOTE]
>
>画像サービング （[!DNL /is/image/*]）および画像レンダリング （[!DNL /ir/render/*]）のクライアントトラフィックに加えて、アクセスログには特定の内部トラフィックが含まれる場合があります。これには、[!DNL Platform Server] カタログシステム （[!DNL /is-catalog/*]）へのアクセス、キャッシュ共有およびエラーリダイレクト要求（[!DNL /is/cache/*]）、[!DNL Platform Server]にデプロイされた他のパッケージ （Dynamic Media ビューア （[!DNL /is-viewers/*]）へのアクセス、静的トラフィックおよび[!DNL Platform Server] （例：[!DNL /is-docs/*]）がサービスを提供する静的コンテンツリクエストが含まれます。

[!DNL /is-catalog]と[!DNL /is/cache]のルートパスを持つリクエストは、常に任意のクライアントトラフィック分析から除外する必要があります。
