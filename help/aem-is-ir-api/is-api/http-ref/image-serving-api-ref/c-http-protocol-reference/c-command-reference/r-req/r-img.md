---
description: Image（初期設定）。 標準の画像データを要求します。
seo-description: Image（初期設定）。 標準の画像データを要求します。
seo-title: img
solution: Experience Manager
title: img
topic: Scene7 Image Serving - Image Rendering API
uuid: 4809f916-0ccf-4a24-a93b-c51ed6203061
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---


# img{#img}

Image（初期設定）。 標準の画像データを要求します。

`req=img`

応答データの形式と応答のMIMEタイプは`fmt=`によって決定されます。 `req=img` はデフォルトのリクエストタイプで、明示的に指定する必要はありません。HTTP応答は、`catalog::Expiration`に基づいてTTLでキャッシュ可能です。

その他の要求コマンドは、ドキュメントに従って適用されます。
