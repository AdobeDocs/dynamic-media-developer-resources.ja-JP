---
description: オプションのロックサフィックスを含むリクエスト文字列の修飾子部分の全体の内容は、標準のbase64 エンコーディングを適用することで不明瞭になる場合があります。
solution: Experience Manager
title: リクエストの難読化
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
TQID: 'https://experienceleague.adobe.com/77Q5rV3cP4KoBz3rFKlEmBlumS0TBthuLbLQBETPitE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 220
ht-degree: 1%

---

# リクエストの難読化{#request-obfuscation}

オプションのロックサフィックスを含むリクエスト文字列の修飾子部分の全体の内容は、標準のbase64 エンコーディングを適用することで不明瞭になる場合があります。

`attribute::RequestObfuscation`が設定されている場合、サーバーはデコードを試みます。 デコードに失敗した場合、リクエストは拒否されます。 リクエストのロックとリクエストの難読化の両方が適用される場合は、base64 エンコーディングの前にロックサフィックスを生成して追加する必要があります。

>[!IMPORTANT]
>
>この機能を有効にした場合、次のような使用に対する特定の制限があることに注意してください。<br>- Dynamic Media ユーザーインターフェイスに、**[!UICONTROL 最終公開日]** フィールドの正しい詳細が表示されない場合があります。 ただし、この影響は公開には影響しません。<br> – 現在、**[!UICONTROL リクエストの難読化]**&#x200B;および&#x200B;**[!UICONTROL リクエストのロック]**&#x200B;が有効になっている場合、HLS ビデオストリーミングは機能しません。<br> – 現在、**[!UICONTROL リクエストの難読化]**&#x200B;および&#x200B;**[!UICONTROL リクエストのロック]**&#x200B;が有効になっている場合、一部のDynamic Media ビューアは機能しません。

## 例 {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

エンコード先：

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

値の文字列に「=」、「&amp;」、「%」が出現した場合は、リクエストを難読化する前に、「%xx」エンコーディングを使用してエスケープする必要があります。 base64 エンコーディングはhttp送信に安全であるため、リクエストのロックが適用されている場合でも、難読化の前または後にリクエストの&#x200B;*modifiers*&#x200B;部分をhttp エンコードする必要はありません。

## 関連項目 {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP エンコーディング &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)、[要求ロック &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c)、[属性：:RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
