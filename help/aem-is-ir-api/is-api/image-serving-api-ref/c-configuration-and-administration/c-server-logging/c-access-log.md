---
description: これは、プラットフォームサーバーに対するすべてのHTTP要求を追跡するプライマリログです。 画像レンダリングを有効にすると、同じファイルにアクセスログデータが書き込まれます。
seo-description: これは、プラットフォームサーバーに対するすべてのHTTP要求を追跡するプライマリログです。 画像レンダリングを有効にすると、同じファイルにアクセスログデータが書き込まれます。
seo-title: アクセスログ
solution: Experience Manager
title: アクセスログ
topic: Scene7 Image Serving - Image Rendering API
uuid: 33cd4338-1fe7-46ac-83f5-200ea26f1e22
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# アクセスログ{#access-log}

これは、プラットフォームサーバーに対するすべてのHTTP要求を追跡するプライマリログです。 画像レンダリングを有効にすると、同じファイルにアクセスログデータが書き込まれます。

アクセスログは、server.xmlで設定されます。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>画像サービング()および画像レンダリング()のクライアント [!DNL /is/image/*]トラフィックに加えて、アクセスログに [!DNL /ir/render/*]は次のような特定の内部トラフィックが含まれる場合があります。プラットフォームサーバのカタログシステム( [!DNL /is-catalog/*])、キャッシュの共有とエラーのリダイレクトの要求( [!DNL /is/cache/*])、Platform Serverに展開された他のパッケージ( Scene7ビューア( [!DNL /is-viewers/*])、静的トラフィック、静的コンテンツの要求(例： [!DNL /is-docs/*])。

およびルートパ [!DNL /is-catalog] スを持つ [!DNL /is/cache] リクエストは、常にクライアントトラフィック分析から除外する必要があります。
