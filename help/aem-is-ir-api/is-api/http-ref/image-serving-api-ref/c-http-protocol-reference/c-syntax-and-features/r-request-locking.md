---
description: 要求に対する改ざんの機会を低減するため、簡単なロック設備を提供する。
solution: Experience Manager
title: リクエストのロック
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# リクエストのロック{#request-locking}

要求に対する改ざんの機会を低減するため、簡単なロック設備を提供する。

attribute::RequestLock が設定されている場合、 `&xxxx`は 4 桁の 16 進値です。 この 16 進数値は、 *修飾子* リクエストの一部（「?」の後） :URL パスを *修飾子*) をクリックします。 これは、リクエストが完全に http エンコードされた後、（オプションで）不明化される前におこなう必要があります。 要求の不明化を解除すると、サーバーは、修飾子文字列に対して同じハッシュアルゴリズムを使用します（ロック値を含む最後の 5 文字を除く）。 生成されたキーがロックと一致しない場合、リクエストは拒否されます。

>[!IMPORTANT]
>
>この機能を有効にする場合、次のような使用に制限があることに注意してください。<br>- Dynamic Mediaユーザーインターフェイスで、 **[!UICONTROL 最終公開日]** フィールドに入力します。 ただし、この影響は公開には影響しません。<br> — 現在、HLS ビデオストリーミングは、 **[!UICONTROL 難読化のリクエスト]** および **[!UICONTROL リクエストのロック]** が有効になっている。<br> — 現在、一部のDynamic Mediaビューアは **[!UICONTROL 難読化のリクエスト]** および **[!UICONTROL リクエストのロック]** が有効になっている。

リクエストロック値を生成する C++サンプルコード：

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

[HTTP エンコーディング](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [難読化のリクエスト](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [attribute::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
