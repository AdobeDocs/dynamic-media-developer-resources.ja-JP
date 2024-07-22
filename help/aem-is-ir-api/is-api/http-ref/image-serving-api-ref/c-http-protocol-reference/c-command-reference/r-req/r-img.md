---
title: img
description: 画像（デフォルト）。 標準画像データをリクエストします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5338358e-755b-41d6-a941-8754d0deb9aa
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 0%

---

# img{#img}

画像（デフォルト）。 標準画像データをリクエストします。

`req=img`

返信データの形式と応答の MIME タイプは、`fmt=` によって決まります。 修飾子 `req=img` はデフォルトのリクエストタイプで、明示的には必要ありません。 HTTP 応答は、`catalog::Expiration` に基づく TTL でキャッシュ可能です。

その他のリクエストコマンドは、ドキュメントに記載されているように適用されます。
