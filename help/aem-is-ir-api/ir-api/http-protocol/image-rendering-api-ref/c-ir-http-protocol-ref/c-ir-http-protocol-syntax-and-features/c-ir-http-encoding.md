---
title: 画像レンダリング HTTP エンコーディング
description: コマンド値は、%xx エスケープシーケンスを使用してhttp エンコードする必要があります。これにより、値の文字列に予約文字'='、'&'および'%'が含まれなくなります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
TQID: 'https://experienceleague.adobe.com/TNB9NbrGzMGS64CxHgj7aXlSHz8-KPBB0hMxB36mKvI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 145
ht-degree: 2%

---

# 画像レンダリング HTTP エンコーディング{#image-rendering-http-encoding}

コマンド値は、%xx エスケープシーケンスを使用してhttp エンコードする必要があります。これにより、値の文字列に予約文字&#39;=&#39;、&#39;&amp;&#39;および&#39;%&#39;が含まれなくなります。

それ以外の場合は、標準のHTTP エンコーディングルールが適用されます。 HTTP仕様では、「」（スペース）、「」（二重引用符）、「#」、「%」、「&lt;」、「>」などの安全でない文字だけでなく、`<return>`や`<tab>`などの制御文字もエンコードする必要があります。

**注意：** リクエストのネスト区切り文字として使用される中かっこ{ }はエンコードしないでください。 一部のメールクライアントでは、埋め込みHTTP リクエストで中括弧をエンコードしています。 この問題が発生した場合、画像レンダリングでは、中括弧の代わりに括弧（）を使用できます。

## 例 {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

上記のリクエストフラグメントは、次のようにエンコードする必要があります。

`…&$text=rate%26weight%3D85%25%2027%23&…`

## 関連項目 {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1仕様（RFC 2616）](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
