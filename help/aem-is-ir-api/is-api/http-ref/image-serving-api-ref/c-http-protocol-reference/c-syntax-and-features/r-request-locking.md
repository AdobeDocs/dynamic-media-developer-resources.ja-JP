---
description: 要求を改ざんする機会を減らすために、単純なロック設備が提供される。
solution: Experience Manager
title: リクエストロック
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# リクエストロック{#request-locking}

要求を改ざんする機会を減らすために、単純なロック設備が提供される。

attribute::RequestLock が設定されている場合、リクエストにロック値を `&xxxx` の形式で付加する必要があります。xxxx は 4 桁の 16 進数値です。 この 16 進数値は、リクエストの *修飾子* 部分（「?」の後）に適用される単純なハッシュアルゴリズムを使用して生成されます URL パスをから分離します *修飾子*）。 これは、リクエストが完全に http エンコードされた後、（オプションで）不明化される前に行う必要があります。 リクエストの難読化を解除した後、サーバーは修飾子の文字列に対して同じハッシュアルゴリズムを使用します（ロック値を含む最後の 5 文字を除く）。 生成されたキーがロックと一致しない場合、リクエストは拒否されます。

>[!IMPORTANT]
>
>この機能を有効にする場合は、次のような使用制限があることに注意してください。<br>- Dynamic Media ユーザーインターフェイスに、「**[!UICONTROL 最終公開日]**」フィールドの正しい詳細が表示されない場合があります。 ただし、この影響は公開には影響しません。<br> – 現在、**[!UICONTROL リクエストの不明化]** および **[!UICONTROL リクエストロック]** が有効になっている場合、HLS ビデオストリーミングは機能しません。<br> – 現在、**[!UICONTROL リクエストの不明化]** および **[!UICONTROL リクエストロック]** が有効になっている場合、一部の Dynamic Media ビューアが機能しません。

C++ リクエストロック値を生成するサンプルコード：

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

[HTTP エンコード ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)、[ 要求の不明化 ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d)、[attribute::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
