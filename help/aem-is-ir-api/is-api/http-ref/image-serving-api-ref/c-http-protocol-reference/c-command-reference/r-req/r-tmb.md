---
description: サムネール画像 カタログのサムネール条件を使用して、形式設定およびサイズ設定された画像データを要求します。
solution: Experience Manager
title: tmb
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 0%

---


# tmb{#tmb}

サムネール画像 カタログのサムネール条件を使用して、形式設定およびサイズ設定された画像データを要求します。

`req=tmb`

応答データの形式と応答のMIMEタイプは`fmt=`によって決定されます。 `fit=`を除くすべてのコマンドをサポートします。

[サムネールの拡大/縮小](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)を参照してください。

HTTP応答は、`catalog::Expiration`に基づいてTTLでキャッシュできます。
