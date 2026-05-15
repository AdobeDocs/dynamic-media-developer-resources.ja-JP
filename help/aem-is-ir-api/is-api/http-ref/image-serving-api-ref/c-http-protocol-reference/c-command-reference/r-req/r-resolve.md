---
title: 解決
description: デバッグリクエスト。 このdebug コマンドは、req=imgと同様に、リクエストの解析と前処理、画像カタログの検索、カタログ修飾子のインクルード、マクロおよび変数置換などを実行します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
TQID: 'https://experienceleague.adobe.com/yS8k6Njz17UK9W42N6wyqmeg3FDweKnZ3vkMNw9wnJI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 2%

---

# 解決{#resolve}

デバッグリクエスト。 このdebug コマンドは、req=imgと同様に、リクエストの解析と前処理、画像カタログの検索の実行、catalog::Modifierのインクルード、マクロと変数の置換などを行います。

`req=resolve`

MIME タイプ `text/plain`を持つ結果画像の代わりに、最後のリクエスト文字列が返されます。

HTTP応答はキャッシュできません。
