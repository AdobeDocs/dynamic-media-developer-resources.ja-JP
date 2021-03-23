---
description: サムネール画像 カタログのサムネール条件を使用して、形式設定およびサイズ設定された画像データを要求します。
seo-description: サムネール画像 カタログのサムネール条件を使用して、形式設定およびサイズ設定された画像データを要求します。
seo-title: tmb
solution: Experience Manager
title: tmb
uuid: 0f098c30-a164-47a6-abb2-0eb1d0bc24da
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---


# tmb{#tmb}

サムネール画像 カタログのサムネール条件を使用して、形式設定およびサイズ設定された画像データを要求します。

`req=tmb`

応答データの形式と応答のMIMEタイプは`fmt=`によって決定されます。 `fit=`を除くすべてのコマンドをサポートします。

[サムネールの拡大/縮小](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)を参照してください。

HTTP応答は、`catalog::Expiration`に基づいてTTLでキャッシュできます。
