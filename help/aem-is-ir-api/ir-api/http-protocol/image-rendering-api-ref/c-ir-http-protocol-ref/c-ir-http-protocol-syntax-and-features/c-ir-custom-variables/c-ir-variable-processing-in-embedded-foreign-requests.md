---
title: 埋め込まれた外部リクエストでの変数処理
description: 埋め込まれた外部リクエストの中かっこ内のどこかで発生する$var$参照は、一致する変数定義値で置き換えられます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
TQID: 'https://experienceleague.adobe.com/-0KT9d6qz9-8d41vKNgbCYUKQQLBRaLE-0TFmyIvRCM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 0%

---

# 埋め込まれた外部リクエストでの変数処理{#variable-processing-in-embedded-foreign-requests}

埋め込まれた外部リクエストの中かっこ内のどこかで発生する`$var$`参照は、一致する変数定義値で置き換えられます。

埋め込まれた外部リクエストを画像カタログ内のテンプレートに配置できます。

サーバーが最終的な外部URLの送信を試みる前に再エンコードが適用されないため、通常、外部リクエストに置換される変数値はダブルエンコードする必要があります。
