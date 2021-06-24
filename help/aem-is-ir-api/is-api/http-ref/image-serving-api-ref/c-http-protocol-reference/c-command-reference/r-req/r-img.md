---
description: 画像（デフォルト） 標準のイメージデータを要求します。
solution: Experience Manager
title: img
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 5338358e-755b-41d6-a941-8754d0deb9aa
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# img{#img}

画像（デフォルト） 標準のイメージデータを要求します。

`req=img`

応答データの形式と応答のMIMEタイプは`fmt=`によって決まります。 `req=img` はデフォルトのリクエストタイプで、明示的に指定する必要はありません。HTTP応答は、`catalog::Expiration`に基づいてTTLでキャッシュ可能です。

その他の要求コマンドは、説明に従って適用されます。
