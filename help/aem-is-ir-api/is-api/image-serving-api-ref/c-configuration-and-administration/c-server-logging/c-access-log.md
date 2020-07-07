---
description: これは、Platformサーバーに対するすべてのHTTP要求を追跡する主要なログです。 画像レンダリングを有効にすると、アクセスログデータが同じファイルに書き込まれます。
seo-description: これは、Platformサーバーに対するすべてのHTTP要求を追跡する主要なログです。 画像レンダリングを有効にすると、アクセスログデータが同じファイルに書き込まれます。
seo-title: アクセスログ
solution: Experience Manager
title: アクセスログ
topic: Scene7 Image Serving - Image Rendering API
uuid: 33cd4338-1fe7-46ac-83f5-200ea26f1e22
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---


# アクセスログ{#access-log}

これは、Platformサーバーに対するすべてのHTTP要求を追跡する主要なログです。 画像レンダリングを有効にすると、アクセスログデータが同じファイルに書き込まれます。

アクセスログは、server.xmlで設定します。

>[!NOTE]
>
>画像サービング( [!DNL /is/image/*])および画像レンダリング( [!DNL /ir/render/*])のクライアントトラフィックに加えて、アクセスログには、次のような特定の内部トラフィックが含まれる場合があります。 Platformサーバカタログシステム( [!DNL /is-catalog/*])へのアクセス、キャッシュ共有とエラーリダイレクトの要求( [!DNL /is/cache/*])、Platformサーバにデプロイされている他のパッケージ( Scene7ビューア( [!DNL /is-viewers/*])、静的トラフィック、Platformサーバが処理する静的コンテンツの要求( [!DNL /is-docs/*])をクリックします。

ルートパス [!DNL /is-catalog][!DNL /is/cache] とルートパスを持つリクエストは、常にクライアントトラフィック分析から除外する必要があります。
