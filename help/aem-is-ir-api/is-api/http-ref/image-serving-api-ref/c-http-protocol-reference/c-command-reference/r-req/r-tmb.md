---
description: サムネール画像 カタログのサムネール条件を使用して、形式設定およびサイズ設定された画像データを要求します。
seo-description: サムネール画像 カタログのサムネール条件を使用して、形式設定およびサイズ設定された画像データを要求します。
seo-title: tmb
solution: Experience Manager
title: tmb
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f098c30-a164-47a6-abb2-0eb1d0bc24da
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# tmb{#tmb}

サムネール画像 カタログのサムネール条件を使用して、形式設定およびサイズ設定された画像データを要求します。

`req=tmb`

応答データの形式と応答のMIMEタイプは、によって決まりま `fmt=`す。 を除くすべてのコマンドをサポートしま `fit=`す。

サムネールの [拡大・縮小を参照してくださ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)い。

HTTP応答は、TTLを基にしてキャッシュできます `catalog::Expiration`。
