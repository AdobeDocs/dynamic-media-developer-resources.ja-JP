---
description: 要求を改ざんする機会を減らすために、簡単なロック設備を提供する。
solution: Experience Manager
title: リクエストのロック
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
TQID: 'https://experienceleague.adobe.com/9icGIK7meNSVUzYnsFBFM-GwG7KLe90bMDuqN89xmMk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 0%

---

# リクエストのロック{#request-locking}

要求を改ざんする機会を減らすために、簡単なロック設備を提供する。

属性：:RequestLockが設定されている場合、ロック値を`&xxxx`形式でリクエストに追加し、xxxxを4桁の16進値にする必要があります。 この16進値は、リクエストの&#x200B;*修飾子*&#x200B;部分（「?」の後に、URL パスを&#x200B;*修飾子*）から分離する単純なハッシュアルゴリズムを使用して生成されます。 これは、リクエストが完全にhttp エンコードされた後で、（オプションで）難読化される前に行う必要があります。 リクエストの難読化解除後、サーバーは修飾子文字列に対して同じハッシュアルゴリズムを使用します（ロック値を含む最後の5文字を除く）。 生成されたキーがロックと一致しない場合、リクエストは拒否されます。

>[!IMPORTANT]
>
>この機能を有効にした場合、次のような使用に対する特定の制限があることに注意してください。<br>- Dynamic Media ユーザーインターフェイスに、**[!UICONTROL 最終公開日]** フィールドの正しい詳細が表示されない場合があります。 ただし、この影響は公開には影響しません。<br> – 現在、**[!UICONTROL リクエストの難読化]**&#x200B;および&#x200B;**[!UICONTROL リクエストのロック]**&#x200B;が有効になっている場合、HLS ビデオストリーミングは機能しません。<br> – 現在、**[!UICONTROL リクエストの難読化]**&#x200B;および&#x200B;**[!UICONTROL リクエストのロック]**&#x200B;が有効になっている場合、一部のDynamic Media ビューアは機能しません。

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

[HTTP エンコーディング ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)、[難読化リクエスト ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d)、[属性：:RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
