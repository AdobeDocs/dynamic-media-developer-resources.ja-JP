---
description: オプションのロックサフィックスを含む、リクエスト文字列の修飾子部分全体の内容は、標準のbase64エンコーディングを適用すると見にくくなる場合があります。
seo-description: オプションのロックサフィックスを含む、リクエスト文字列の修飾子部分全体の内容は、標準のbase64エンコーディングを適用すると見にくくなる場合があります。
seo-title: 不明化のリクエスト
solution: Experience Manager
title: 不明化のリクエスト
topic: Scene7 Image Serving - Image Rendering API
uuid: 59b12a78-c4ba-4b6d-97bc-63150298ed73
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 不明化のリクエスト{#request-obfuscation}

オプションのロックサフィックスを含む、リクエスト文字列の修飾子部分全体の内容は、標準のbase64エンコーディングを適用すると見にくくなる場合があります。

が設定されている場合、サーバーはデコード `attribute::RequestObfuscation` を試行します。 デコードに失敗すると、要求は拒否されます。 リクエストのロックとリクエストの不明化の両方が適用される場合は、ロックのサフィックスを生成し、base64エンコーディングの前に追加する必要があります。

## 例 {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

エンコード先：

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

値文字列内の「=」、「&amp;」および「%」は、リクエストを不明化する前に、「%xx」エンコーディングを使用してエスケープする必要があります。 リクエストのロックが適用されている場合でも、リクエストの修飾子の一部を不明化の前後に ** 、httpエンコードする必要はありません。base64のエンコードはHTTP送信に安全なのです。

## 関連項目 {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP Encoding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Request Locking](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c), [attribute::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
