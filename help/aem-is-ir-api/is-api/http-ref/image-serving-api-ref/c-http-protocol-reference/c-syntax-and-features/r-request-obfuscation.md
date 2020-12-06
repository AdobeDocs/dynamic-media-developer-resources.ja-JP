---
description: オプションのロックサフィックスを含む、リクエスト文字列の修飾子部分全体の内容は、標準のbase64エンコーディングを適用すると見にくくなる場合があります。
seo-description: オプションのロックサフィックスを含む、リクエスト文字列の修飾子部分全体の内容は、標準のbase64エンコーディングを適用すると見にくくなる場合があります。
seo-title: 不明化のリクエスト
solution: Experience Manager
title: 不明化のリクエスト
topic: Scene7 Image Serving - Image Rendering API
uuid: 59b12a78-c4ba-4b6d-97bc-63150298ed73
translation-type: tm+mt
source-git-commit: 021c1d1f975083af3950775e230d4f73cbf9e0ec
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 1%

---


# 不明化のリクエスト{#request-obfuscation}

オプションのロックサフィックスを含む、リクエスト文字列の修飾子部分全体の内容は、標準のbase64エンコーディングを適用すると見にくくなる場合があります。

が設定されている場合、サーバーはデコード `attribute::RequestObfuscation` を試行します。 デコードが失敗すると、要求は拒否されます。 要求ロックと要求の不明化の両方が適用される場合は、ロックサフィックスを生成して、base64エンコーディングの前に追加する必要があります。

>[!IMPORTANT]
>
>この機能を有効にする場合、使用には次のような制限があることに注意してください。<br>— ダイナミックメディアユーザーインターフェイスには、 **[!UICONTROL 最後に公開された]** フィールドの正しい詳細が表示されない場合があります。 ただし、この影響は投稿には影響しません。<br>— 現在、**[!UICONTROL 要求の不明化]**&#x200B;と **[!UICONTROL 要求のロックが有効な場合、HLSビデオストリーミングは機能しません]** 。<br>— 現在、 **[!UICONTROL 要求の不明化と要求のロックが有効になっていると、一部のダイナミックメディアビューアが機能しません]****** 。

## 例 {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

エンコード先：

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

値文字列内の「=」、「&amp;」および「%」は、エンコード「%xx」を使用してエスケープする必要があります。エスケープが行われないと、リクエストが不明化されます。 base64エンコーディングはHTTP送信に安全なので、リクエストのロックが適用されている場合でも、不明化の前または後に、リクエストの *modifiers* 部分をHTTPエンコードする必要はありません。

## 関連項目 {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTPエンコーディング](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)、 [要求ロック](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c)、 [attribute::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
