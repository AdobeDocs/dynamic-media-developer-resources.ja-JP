---
title: JSONP プロパティ
description: 応答形式として jsonp を指定した場合、返信データは JSONP（パディング付き JavaScript Object Notation）を使用して形式設定され、JavaScript 関数呼び出しでラップされます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: d1df6e943747f9db12c08003647aee840fdfcc0a
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---

# JSONP プロパティ{#jsonp-properties}

応答形式として jsonp を指定した場合、返信データは JSONP（パディング付き JavaScript Object Notation）を使用して形式設定され、JavaScript 関数呼び出しでラップされます。

クライアントは、オプションで一意のリクエスト識別子 ( *`reqId`*) と呼ばれ、応答で返されます。これにより、クライアントは非同期で受信した複数の応答を区別できます。 一般的な応答の一般的な構造は次のとおりです。

```
/*jsonp*/s7jsonResponse({ 
   " 
<varname>
  objectName 
</varname>. 
<varname>
  propertyName 
</varname>" : " 
<varname>
  propertyValue 
</varname>", 
   ... 
 }, " 
<varname>
  reqId 
</varname>" );
```

この `s7jsonResponse` JavaScript 関数は、クライアントによって定義される必要があります。 最も簡単な形式では、関数は次のようになります。

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

JSONP 応答形式をサポートするリクエストでは、の拡張構文を使用して JS コールバックハンドラーの名前を指定できます。 `req=` パラメーター：

`req=...,json [&handler = reqHandler]`

この `<reqHandler>` 構文は、JSONP 応答に存在する JS ハンドラーの名前です。 a ～ z、A ～ Z、0 ～ 9 文字のみ使用できます。 オプション。初期設定は `s7jsonResponse`.

Dynamic Mediaの画像サービングビューアパッケージには、画像サービングから JSONP 形式のデータを要求して解析するユーティリティが含まれています。

詳しくは、 [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) を参照してください。

詳しくは、 [www.json.org](https://www.json.org/json-en.html) を参照してください。

関連トピック [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
