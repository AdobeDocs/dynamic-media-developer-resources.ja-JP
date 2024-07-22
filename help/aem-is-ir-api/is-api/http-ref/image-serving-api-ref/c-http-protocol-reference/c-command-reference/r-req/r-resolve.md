---
title: 解決
description: デバッグリクエスト。 この debug コマンドは、req=img と同様に、リクエストの解析と前処理、画像カタログ検索、カタログ修飾子の包含、マクロおよび変数の置換などの実行を行います。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 2%

---

# 解決{#resolve}

デバッグリクエスト。 この debug コマンドは、req=img と同様に、リクエストの解析と前処理、画像カタログの検索、catalog::Modifier の包含、マクロと変数の置換などを実行します。

`req=resolve`

結果の画像ではなく、MIME タイプ `text/plain` の最終的なリクエスト文字列が返されます。

HTTP 応答はキャッシュできません。
