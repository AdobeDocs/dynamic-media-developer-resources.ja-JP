---
description: これは、プラットフォームサーバーに対するすべてのHTTP要求を追跡する主要なログです。 画像レンダリングを有効にすると、アクセスログデータが同じファイルに書き込まれます。
seo-description: これは、プラットフォームサーバーに対するすべてのHTTP要求を追跡する主要なログです。 画像レンダリングを有効にすると、アクセスログデータが同じファイルに書き込まれます。
seo-title: アクセスログ
solution: Experience Manager
title: アクセスログ
uuid: 33cd4338-1fe7-46ac-83f5-200ea26f1e22
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---


# アクセスログ{#access-log}

これは、プラットフォームサーバーに対するすべてのHTTP要求を追跡する主要なログです。 画像レンダリングを有効にすると、アクセスログデータが同じファイルに書き込まれます。

アクセスログは、server.xmlで設定します。

>[!NOTE]
>
>画像サービング([!DNL /is/image/*])および画像レンダリング([!DNL /ir/render/*])のクライアントトラフィックに加えて、アクセスログには、次のような特定の内部トラフィックが含まれる場合があります。Platform Serverカタログシステム([!DNL /is-catalog/*])、キャッシュの共有とエラーのリダイレクトの要求([!DNL /is/cache/*])、Dynamic Mediaビューア([!DNL /is-viewers/*])、静的トラフィック、プラットフォームサーバーが処理する静的コンテンツの要求([!DNL /is-docs/*])。

[!DNL /is-catalog]と[!DNL /is/cache]のルートパスを持つリクエストは、常にクライアントトラフィック分析から除外する必要があります。
