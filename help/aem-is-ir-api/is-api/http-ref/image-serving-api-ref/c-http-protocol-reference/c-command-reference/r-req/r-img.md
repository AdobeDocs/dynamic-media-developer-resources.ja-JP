---
description: 画像（デフォルト） 標準の画像データを要求します。
seo-description: 画像（デフォルト） 標準の画像データを要求します。
seo-title: img
solution: Experience Manager
title: img
topic: Scene7 Image Serving - Image Rendering API
uuid: 4809f916-0ccf-4a24-a93b-c51ed6203061
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# img{#img}

画像（デフォルト） 標準の画像データを要求します。

`req=img`

応答データの形式と応答のMIMEタイプは、によって決定されま `fmt=`す。 `req=img` はデフォルトのリクエストタイプで、明示的に指定する必要はありません。 The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

その他のリクエストコマンドは、ドキュメントに記載されているとおりに適用されます。
