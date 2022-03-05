---
title: 画像レンダリング HTTP エンコーディング
description: コマンド値は、値文字列に予約文字「=」、「&」および「%」が含まれないように、%xx エスケープシーケンスを使用して HTTP エンコードする必要があります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---

# 画像レンダリング HTTP エンコーディング{#image-rendering-http-encoding}

コマンド値は、値文字列に予約文字「=」、「&amp;」および「%」が含まれないように、%xx エスケープシーケンスを使用して HTTP エンコードする必要があります。

それ以外の場合は、標準の HTTP エンコーディングルールが適用されます。 HTTP の仕様では、「 」（スペース）、「」（二重引用符）、「#」、「%」、「&lt;」、「>」などの安全でない文字と、次のような制御文字をエンコードする必要があります。 `<return>` および `<tab>`.

**注意：** リクエストをネストする区切り文字として中括弧 { } を使用する場合は、エンコードしないでください。 一部の電子メールクライアントは、埋め込み HTTP リクエストで中括弧をエンコードしています。 この問題が発生した場合、画像レンダリングでは中括弧の代わりに括弧 ( ) を使用できます。

## 例 {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

上記の要求フラグメントは、次のようにエンコードする必要があります。

`…&$text=rate%26weight%3D85%25%2027%23&…`

## 関連項目 {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1 仕様 (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
