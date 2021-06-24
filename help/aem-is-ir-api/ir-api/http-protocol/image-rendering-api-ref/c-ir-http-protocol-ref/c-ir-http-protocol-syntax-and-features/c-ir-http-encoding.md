---
description: コマンド値は、値文字列に予約文字「=」、「&」、「%」が含まれないように、%xxエスケープシーケンスを使用してHTTPエンコードする必要があります。
solution: Experience Manager
title: 画像レンダリングHTTPエンコーディング
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# 画像レンダリングHTTPエンコーディング{#image-rendering-http-encoding}

コマンド値は、値文字列に予約文字「=」、「&amp;」、「%」が含まれないように、%xxエスケープシーケンスを使用してHTTPエンコードする必要があります。

それ以外の場合は、標準のHTTPエンコーディングルールが適用されます。 HTTPの仕様では、「 」（スペース）、「」（二重引用符）、「#」、「%」、「&lt;」、「>」などの安全でない文字と、`<return>`や`<tab>`などの制御文字をエンコードする必要があります。

**注意：** リクエストのネスト区切り文字として使用される波括弧{ }はエンコードしないでください。一部の電子メールクライアントは、埋め込みHTTPリクエスト内で波括弧をエンコードしています。 これが問題となる場合、画像レンダリングでは中括弧( )を中括弧ではなく使用できます。

## 例 {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

上記の要求フラグメントは、次のようにエンコードする必要があります。

`…&$text=rate%26weight%3D85%25%2027%23&…`

## 関連項目 {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1仕様(RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
