---
description: サムネール画像。 カタログサムネール条件を使用して書式設定およびサイズ設定された画像データをリクエストします。
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9bdcc1c4-fe2b-4316-a472-07a533f105a0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 0%

---

# tmb{#tmb}

サムネール画像。 カタログサムネール条件を使用して書式設定およびサイズ設定された画像データをリクエストします。

`req=tmb`

返信データの形式と応答の MIME タイプは、`fmt=` によって決まります。 `fit=` を除くすべてのコマンドをサポートします。

[&#x200B; サムネールの拡大・縮小 &#x200B;](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f) を参照してください。

`catalog::Expiration` に基づいて、HTTP 応答を TTL と共にキャッシュできます。
