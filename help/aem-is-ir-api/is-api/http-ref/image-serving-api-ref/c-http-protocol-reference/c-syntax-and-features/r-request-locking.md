---
description: 要求に対する改ざんの機会を低減するために、簡単なロック設備を備える。
seo-description: 要求に対する改ざんの機会を低減するために、簡単なロック設備を備える。
seo-title: 要求のロック
solution: Experience Manager
title: 要求のロック
topic: Scene7 Image Serving - Image Rendering API
uuid: 03239376-1e40-48d2-a396-c276802854ed
translation-type: tm+mt
source-git-commit: 80ae3a549340156bb74faa1793c43d3a8fa3853c
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# 要求のロック{#request-locking}

要求に対する改ざんの機会を低減するために、簡単なロック設備を備える。

attribute::RequestLockが設定されている場合、ロック値をリクエストに追加する必要があります。 `&xxxx`形式はxxxで、4桁の16進値を表します。 この16進値は、リクエストの *modifiers* 部分に適用される単純なハッシュアルゴリズムを使用して生成されます（「?」の後）。 」をクリックします。これは、URLパスと *修飾子を区切るものです*)。 この処理は、リクエストが完全にHTTPエンコードされた後、不明化される前に行う必要があります（オプション）。 リクエストの不明化を解除した後、サーバは修飾子文字列に対して同じハッシュアルゴリズムを使用します（ロック値を含む最後の5文字を除く）。 生成されたキーがロックと一致しない場合、要求は拒否されます。

>[!IMPORTANT]
>
>この機能を有効にした場合、使用には次のような制限があることに注意してください。<br>— ダイナミックメディアユーザーインターフェイスには、 **[!UICONTROL 最後に公開された]** フィールドの正しい詳細が表示されない場合があります。 ただし、この影響は投稿には影響しません。<br>— 現在、「**[!UICONTROL 要求の不明化]**」と「 **[!UICONTROL 要求のロック]** 」が有効な場合、HLSビデオストリーミングは機能しません。

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

[HTTPエンコーディング](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)、 [要求の不明化](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d)、 [attribute::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
