---
description: これは、 [!DNL Platform Server] に対して行われたすべての HTTP リクエストを追跡するプライマリログです。 画像レンダリングを有効にすると、アクセスログデータが同じファイルに書き込まれます。
solution: Experience Manager
title: アクセスログ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# アクセスログ{#access-log}

これは、[!DNL Platform Server] に対して行われたすべての HTTP リクエストを追跡するプライマリログです。 画像レンダリングを有効にすると、アクセスログデータが同じファイルに書き込まれます。

アクセスログは、server.xml で設定されます。

>[!NOTE]
>
>画像サービング用のクライアントトラフィック（[!DNL /is/image/*]）と画像レンダリング用のクライアントトラフィック（[!DNL /ir/render/*]）に加えて、アクセスログには、特定の内部トラフィックが含まれる場合があります。[!DNL Platform Server] カタログシステムへのアクセス（[!DNL /is-catalog/*]）、キャッシュ共有およびエラーリダイレクトリクエスト（[!DNL /is/cache/*]）、Dynamic Media ビューアなどの [!DNL Platform Server] にデプロイされた他のパッケージへのアクセス（[!DNL /is-viewers/*]）、[!DNL Platform Server] が提供する静的トラフィックおよび静的コンテンツリクエスト（[!DNL /is-docs/*] など）です。

[!DNL /is-catalog] および [!DNL /is/cache] のルートパスを持つリクエストは、常にクライアントトラフィック分析から除外する必要があります。
