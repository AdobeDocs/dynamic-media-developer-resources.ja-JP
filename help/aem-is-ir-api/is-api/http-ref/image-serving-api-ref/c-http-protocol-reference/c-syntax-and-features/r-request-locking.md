---
description: 要求に対する改ざんの機会を減らすために、簡単なロック設備を設ける。
seo-description: 要求に対する改ざんの機会を減らすために、簡単なロック設備を設ける。
seo-title: 要求のロック
solution: Experience Manager
title: 要求のロック
topic: Scene7 Image Serving - Image Rendering API
uuid: 03239376-1e40-48d2-a396-c276802854ed
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 要求のロック{#request-locking}

要求に対する改ざんの機会を減らすために、簡単なロック設備を設ける。

attribute::RequestLockが設定されている場合は、ロック値をの形式でリクエストに追加する必要があります。 `&xxxx`xxxxは4桁の16進値です。 この16進数値は、リクエストの修飾子部分に適用される ** （「?」の後）単純なハッシュアルゴリズムを使用して生成されます。 を参照してく *ださい*)。 これは、リクエストが完全にhttpエンコードされた後で行う必要がありますが、不明化される前に（オプションで）行う必要があります。 要求の不明化を解除した後、サーバは修飾子文字列に対して同じハッシュアルゴリズムを使用します（ロック値を含む最後の5文字を除く）。 生成されたキーがロックと一致しない場合、要求は拒否されます。

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

[HTTP Encoding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Request Obfuscation](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [attribute::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
