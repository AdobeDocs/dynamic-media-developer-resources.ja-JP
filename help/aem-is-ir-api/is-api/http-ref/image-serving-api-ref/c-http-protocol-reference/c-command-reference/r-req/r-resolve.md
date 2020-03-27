---
description: デバッグ要求。 このdebugコマンドは、req=imgと同様に、リクエストの解析と前処理、画像カタログの検索、カタログ修飾子の挿入、マクロと変数の置換などを実行します。
seo-description: デバッグ要求。 このdebugコマンドは、req=imgと同様に、リクエストの解析と前処理、画像カタログの検索、カタログ修飾子の挿入、マクロと変数の置換などを実行します。
seo-title: 解決
solution: Experience Manager
title: 解決
topic: Scene7 Image Serving - Image Rendering API
uuid: bd1576a7-4802-4a87-b1c0-406f51382561
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 解決{#resolve}

デバッグ要求。 このdebugコマンドは、req=imgと同様に、リクエストの解析と前処理、画像カタログ参照、catalog::Modifier包含、マクロ置換、変数置換などを実行します。

`req=resolve`

結果の画像の代わりに、MIMEタイプを持つ最終的な要求文字列が返されま `text/plain`す。

HTTP応答はキャッシュできません。
