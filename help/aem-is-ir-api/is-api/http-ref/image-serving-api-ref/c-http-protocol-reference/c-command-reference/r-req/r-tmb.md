---
description: サムネイル画像： カタログのサムネール条件を使用して、フォーマットおよびサイズが設定された画像データをリクエストします。
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9bdcc1c4-fe2b-4316-a472-07a533f105a0
TQID: 'https://experienceleague.adobe.com/z4QJcR89OAXysP9RV9tZ05ipva3j0CpJYjIzL0KWCnI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 55
ht-degree: 0%

---

# tmb{#tmb}

サムネイル画像： カタログのサムネール条件を使用して、フォーマットおよびサイズが設定された画像データをリクエストします。

`req=tmb`

返信データの形式と応答のMIME タイプは、`fmt=`によって決まります。 `fit=`を除くすべてのコマンドをサポートします。

[ サムネールの拡大・縮小](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)を参照してください。

HTTP応答は、`catalog::Expiration`に基づいてTTLでキャッシュできます。
