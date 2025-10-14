---
description: オプションのロックサフィックスを含むリクエスト文字列の修飾子部分全体の内容は、標準の base64 エンコーディングを適用すると不明瞭になる場合があります。
solution: Experience Manager
title: リクエストの不明化
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 1%

---

# リクエストの不明化{#request-obfuscation}

オプションのロックサフィックスを含むリクエスト文字列の修飾子部分全体の内容は、標準の base64 エンコーディングを適用すると不明瞭になる場合があります。

`attribute::RequestObfuscation` が設定されている場合、サーバーはデコードを試みます。 デコードが失敗した場合、リクエストは拒否されます。 リクエストのロックと不明化の両方が適用される場合は、base64 エンコーディングの前にロックサフィックスを生成して追加する必要があります。

>[!IMPORTANT]
>
>この機能を有効にする場合は、次のような使用制限があることに注意してください。<br>- Dynamic Media ユーザーインターフェイスに、「**[!UICONTROL 最終公開日]**」フィールドの正しい詳細が表示されない場合があります。 ただし、この影響は公開には影響しません。<br> – 現在、**[!UICONTROL リクエストの不明化]** および **[!UICONTROL リクエストロック]** が有効になっている場合、HLS ビデオストリーミングは機能しません。<br> – 現在、**[!UICONTROL リクエストの不明化]** および **[!UICONTROL リクエストロック]** が有効になっている場合、一部の Dynamic Media ビューアが機能しません。

## 例 {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

以下にエンコード：

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

値文字列内で&#39;=&#39;、&#39;&amp;&#39;、&#39;%&#39;が見つかった場合は、要求を難読化する前に&#39;%xx&#39; エンコーディングを使用してエスケープする必要があります。 それ以外の場合は、リクエストロックが適用されていても、不明化の前または後にリクエストの一部 *modifiers* を http エンコードする必要はありません。base64 エンコーディングは http 送信に対して安全なためです。

## 関連項目 {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP エンコード &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)、[&#x200B; 要求のロック &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c)、[attribute::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
