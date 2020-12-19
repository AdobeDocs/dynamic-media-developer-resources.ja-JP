---
description: コマンド値は、値文字列に予約文字「=」、「&」、「%」が含まれないように、%xxエスケープシーケンスを使用してHTTPエンコードする必要があります。
seo-description: コマンド値は、値文字列に予約文字「=」、「&」、「%」が含まれないように、%xxエスケープシーケンスを使用してHTTPエンコードする必要があります。
seo-title: 画像レンダリングのHTTPエンコーディング
solution: Experience Manager
title: 画像レンダリングのHTTPエンコーディング
topic: Scene7 Image Serving - Image Rendering API
uuid: 37bd0040-7bad-4548-ab39-7f598a217732
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---


# 画像レンダリングHTTPエンコーディング{#image-rendering-http-encoding}

コマンド値は、値文字列に予約文字「=」、「&amp;」、「%」が含まれないように、%xxエスケープシーケンスを使用してHTTPエンコードする必要があります。

それ以外の場合は、標準のHTTPエンコーディングルールが適用されます。 HTTPの仕様では、&#39; &#39;（スペース）、&#39;&#39;(重複引用符)、&#39;#&#39;、&#39;%&#39;、&#39;&lt;&#39;、&#39;>&#39;などの安全でない文字と、`<return>`や`<tab>`などの制御文字をエンコードする必要があります。

**注意：要求の入れ子の区切り文字として使用される** 波括弧{ }はエンコードできません。一部の電子メールクライアントは、埋め込まれたHTTP要求では中括弧をエンコードしています。 この問題が発生する場合、画像レンダリングでは波括弧の代わりに丸括弧()を使用できます。

## 例 {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

上記の要求フラグメントは、次のようにエンコードする必要があります。

`…&$text=rate%26weight%3D85%25%2027%23&…`

## 関連項目 {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1仕様(RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
