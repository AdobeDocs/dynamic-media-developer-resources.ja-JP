---
description: これは、Platformサーバーに対しておこなわれたすべてのHTTPリクエストを追跡するプライマリログです。 画像レンダリングが有効な場合、アクセスログデータを同じファイルに書き込みます。
solution: Experience Manager
title: アクセスログ
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# アクセスログ{#access-log}

これは、Platformサーバーに対しておこなわれたすべてのHTTPリクエストを追跡するプライマリログです。 画像レンダリングが有効な場合、アクセスログデータを同じファイルに書き込みます。

アクセスログはserver.xmlで設定します。

>[!NOTE]
>
>画像サービング([!DNL /is/image/*])と画像レンダリング([!DNL /ir/render/*])のクライアントトラフィックに加えて、アクセスログには、次のような特定の内部トラフィックが含まれる場合があります。Platform Serverカタログシステム([!DNL /is-catalog/*])へのアクセス、キャッシュの共有とエラーのリダイレクト要求([!DNL /is/cache/*])、Dynamic Mediaビューア([!DNL /is-viewers/*])、Platform Serverが処理する静的トラフィックおよび静的コンテンツ要求(例：[!DNL /is-docs/*])に置き換えます。

[!DNL /is-catalog]と[!DNL /is/cache]のルートパスを持つリクエストは、常にクライアントトラフィック分析から除外する必要があります。
