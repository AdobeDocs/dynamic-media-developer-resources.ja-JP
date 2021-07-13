---
description: 要求の改ざんの機会を減らすために、簡単なロック設備を提供する。
solution: Experience Manager
title: リクエストロック
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# リクエストロック{#request-locking}

要求の改ざんの機会を減らすために、簡単なロック設備を提供する。

attribute::RequestLockが設定されている場合、ロック値を`&xxxx`の形式でリクエストに追加する必要があります。xxxxは4桁の16進値です。 この16進数値は、リクエストの&#x200B;*modifiers*&#x200B;部分に適用される単純なハッシュアルゴリズムを使用して生成されます(「?」 URLパスを&#x200B;*修飾子*&#x200B;から区切ります。 これは、リクエストが完全にHTTPエンコードされた後、（オプションで）不明化される前におこなう必要があります。 要求の不明化を解除すると、サーバーは修飾子文字列に対して同じハッシュアルゴリズムを使用します（ロック値を含む最後の5文字を除く）。 生成されたキーがロックと一致しない場合、リクエストは拒否されます。

>[!IMPORTANT]
>
>この機能を有効にする場合、使用には次のような制限があります。<br>- Dynamic Mediaユーザーインターフェイスに「**[!UICONTROL 最終公開日]**」フィールドの正しい詳細が表示されない場合があります。 ただし、この影響はパブリッシュには影響しません。<br> — 現在、要求の難読化と要求のロック化が有効な場合、HLSビデオス&#x200B;**[!UICONTROL トリー]** ミングは機 **[!UICONTROL 能し]** ません。<br> — 現在、要求の難読化と要求のロックが有効な場合、一部のDynamic Media **[!UICONTROL ビューア]** は機能しま **** せん。

リクエストロック値を生成するC++サンプルコード：

```
unsigned int lockValue(const char *str) 
{ 
    unsigned int sum = 0; 
    if (str == NULL) 
        return sum; 
    for (; *str; ++str) 
        sum = (sum*131 + *str) & 0xffff; 
    return sum; 
} 
```

## 関連項目 {#section-a6d45406c0354669ac581793e4fa8436}

[HTTPエンコーディング](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)、 [リクエストの難読化](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d)、 [attribute::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
