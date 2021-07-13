---
description: デバッグリクエスト。 このdebugコマンドは、req=imgと同様に、要求の解析と前処理、画像カタログ検索の実行、カタログ修飾子の挿入、マクロと変数の置換などを行います。
solution: Experience Manager
title: 解決
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 2%

---

# 解決{#resolve}

デバッグリクエスト。 このdebugコマンドは、req=imgと同様に、要求の解析と前処理、画像カタログ検索の実行、catalog::Modifier inclusions、マクロと変数の置換などを行います。

`req=resolve`

結果の画像の代わりに、MIMEタイプ`text/plain`の最終的な要求文字列が返されます。

HTTP応答はキャッシュできません。
