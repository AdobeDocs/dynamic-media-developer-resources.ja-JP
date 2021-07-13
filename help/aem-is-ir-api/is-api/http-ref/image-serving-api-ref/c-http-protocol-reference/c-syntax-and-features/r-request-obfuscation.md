---
description: オプションのロックサフィックスを含む、要求文字列の修飾子部分全体の内容は、標準のbase64エンコーディングを適用することで隠される場合があります。
solution: Experience Manager
title: 難読化のリクエスト
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---

# 難読化のリクエスト{#request-obfuscation}

オプションのロックサフィックスを含む、要求文字列の修飾子部分全体の内容は、標準のbase64エンコーディングを適用することで隠される場合があります。

`attribute::RequestObfuscation`が設定されている場合、サーバはデコードを試みます。 デコードが失敗すると、要求は拒否されます。 リクエストのロックとリクエストの難読化の両方が適用される場合、ロックサフィックスを生成して、base64エンコーディングの前に追加する必要があります。

>[!IMPORTANT]
>
>この機能を有効にする場合、使用には次のような制限があります。<br>- Dynamic Mediaユーザーインターフェイスに「**[!UICONTROL 最終公開日]**」フィールドの正しい詳細が表示されない場合があります。 ただし、この影響はパブリッシュには影響しません。<br> — 現在、要求の難読化と要求のロック化が有効な場合、HLSビデオス&#x200B;**[!UICONTROL トリー]** ミングは機 **[!UICONTROL 能し]** ません。<br> — 現在、要求の難読化と要求のロックが有効な場合、一部のDynamic Media **[!UICONTROL ビューア]** は機能しま **** せん。

## 例 {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

エンコード先：

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

値文字列内の「=」、「&amp;」および「%」の出現箇所は、要求を不明化する前に、「%xx」エンコーディングを使用してエスケープする必要があります。 base64エンコーディングはhttp送信に安全なので、難読化の前または後に、要求の&#x200B;*modifiers*&#x200B;部分をhttpエンコードする必要はありません。

## 関連項目 {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTPエンコーディング](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)、 [リクエストロック](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c)、 [attribute::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
