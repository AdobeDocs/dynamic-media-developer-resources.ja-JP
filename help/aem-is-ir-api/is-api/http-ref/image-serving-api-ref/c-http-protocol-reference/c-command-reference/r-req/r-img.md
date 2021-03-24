---
description: Image（初期設定）。 標準の画像データを要求します。
solution: Experience Manager
title: img
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 0%

---


# img{#img}

Image（初期設定）。 標準の画像データを要求します。

`req=img`

応答データの形式と応答のMIMEタイプは`fmt=`によって決定されます。 `req=img` はデフォルトのリクエストタイプで、明示的に指定する必要はありません。HTTP応答は、`catalog::Expiration`に基づいてTTLでキャッシュ可能です。

その他の要求コマンドは、ドキュメントに従って適用されます。
