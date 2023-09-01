---
title: 解決
description: デバッグリクエスト。 この debug コマンドは、req=img と同様に、要求の解析と前処理、画像カタログ参照の実行、カタログ修飾子の挿入、マクロと変数の置換などを行います。
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

デバッグリクエスト。 この debug コマンドは、req=img と同様に、要求の解析と前処理、画像カタログ参照の実行、catalog::Modifier インクルージョン、マクロと変数の置き換えなどを行います。

`req=resolve`

結果の画像の代わりに、MIME タイプを持つ最終的な要求文字列が返されます `text/plain`.

HTTP 応答はキャッシュできません。
