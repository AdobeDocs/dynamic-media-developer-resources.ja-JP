---
title: JSONP プロパティ
description: 応答形式に jsonp を指定すると、返信データは JSONP （JavaScript Object Notation with Padding）を使用して書式設定され、JavaScript関数呼び出しでラップされます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: d1df6e943747f9db12c08003647aee840fdfcc0a
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# JSONP プロパティ{#jsonp-properties}

応答形式に jsonp を指定すると、返信データは JSONP （JavaScript Object Notation with Padding）を使用して書式設定され、JavaScript関数呼び出しでラップされます。

クライアントは、オプションで一意のリクエスト識別子（*`reqId`*）を指定できます。この識別子は応答で返され、クライアントは非同期で受信した複数の応答を区別できます。 一般的な応答は、次のような一般的な構造になっています。

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

`s7jsonResponse` JavaScript関数は、クライアントで定義する必要があります。 最も単純な形式では、関数は次のようになります。

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

JSONP 応答形式をサポートするリクエストでは、パラメーターの拡張構文を使用して JS コールバックハンドラーの名前 `req=` 指定できます。

`req=...,json [&handler = reqHandler]`

`<reqHandler>` 構文は、JSONP 応答に存在する JS ハンドラーの名前です。 a ～ z、A ～ Z、0 ～ 9 文字のみを使用できます。 オプション。 デフォルトは `s7jsonResponse` です。

Dynamic Media 画像サービングビューアパッケージには、画像サービングから JSONP 形式のデータを要求および解析するユーティリティが含まれています。

JSONP 形式について詳しくは、[https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) を参照してください。

JSON 形式について詳しくは、[www.json.org](https://www.json.org/json-en.html) を参照してください。

[req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) も参照してください。
