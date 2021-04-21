---
description: これは、プラットフォームサーバーに対するすべてのHTTP要求を追跡する主要なログです。 画像レンダリングを有効にすると、アクセスログデータが同じファイルに書き込まれます。
solution: Experience Manager
title: アクセスログ
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# アクセスログ{#access-log}

これは、プラットフォームサーバーに対するすべてのHTTP要求を追跡する主要なログです。 画像レンダリングを有効にすると、アクセスログデータが同じファイルに書き込まれます。

アクセスログは、server.xmlで設定します。

>[!NOTE]
>
>画像サービング([!DNL /is/image/*])および画像レンダリング([!DNL /ir/render/*])のクライアントトラフィックに加えて、アクセスログには、次のような特定の内部トラフィックが含まれる場合があります。Platform Serverカタログシステム([!DNL /is-catalog/*])、キャッシュの共有とエラーのリダイレクトの要求([!DNL /is/cache/*])、Dynamic Mediaビューア([!DNL /is-viewers/*])、静的トラフィック、プラットフォームサーバーが処理する静的コンテンツの要求([!DNL /is-docs/*])。

[!DNL /is-catalog]と[!DNL /is/cache]のルートパスを持つリクエストは、常にクライアントトラフィック分析から除外する必要があります。
