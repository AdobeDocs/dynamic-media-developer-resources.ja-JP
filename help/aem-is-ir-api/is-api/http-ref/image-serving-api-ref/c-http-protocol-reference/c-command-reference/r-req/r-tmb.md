---
description: サムネール画像。 カタログのサムネール条件を使用して、形式設定およびサイズ設定された画像データを要求します。
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 9bdcc1c4-fe2b-4316-a472-07a533f105a0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# tmb{#tmb}

サムネール画像。 カタログのサムネール条件を使用して、形式設定およびサイズ設定された画像データを要求します。

`req=tmb`

応答データの形式と応答のMIMEタイプは`fmt=`によって決まります。 `fit=`を除くすべてのコマンドをサポートします。

[サムネールの拡大/縮小](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)を参照してください。

HTTP応答は、`catalog::Expiration`に基づいてTTLを使用してキャッシュできます。
