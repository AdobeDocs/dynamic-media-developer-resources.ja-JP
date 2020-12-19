---
description: デバッグ要求。 このdebugコマンドは、req=imgのように、リクエストの解析と前処理、画像カタログ参照の実行、カタログ修飾子の選択、マクロや変数の置換などを行います。
seo-description: デバッグ要求。 このdebugコマンドは、req=imgのように、リクエストの解析と前処理、画像カタログ参照の実行、カタログ修飾子の選択、マクロや変数の置換などを行います。
seo-title: 解決
solution: Experience Manager
title: 解決
topic: Scene7 Image Serving - Image Rendering API
uuid: bd1576a7-4802-4a87-b1c0-406f51382561
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 2%

---


# 解決{#resolve}

デバッグ要求。 このdebugコマンドは、req=imgと同様に、リクエストの解析や前処理、画像カタログ参照の実行、catalog::Modifier選択、マクロや変数の置換などを行います。

`req=resolve`

結果の画像の代わりに、MIMEタイプ`text/plain`の最終要求文字列が返されます。

HTTP応答はキャッシュできません。
