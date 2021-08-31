---
description: 応答形式としてjsonpを指定した場合、応答データはJSONP(JavaScript Object Notation with Padding)を使用して形式設定され、JavaScript関数呼び出しでラップされます。
solution: Experience Manager
title: JSONPプロパティ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 1%

---

# JSONPプロパティ{#jsonp-properties}

応答形式としてjsonpを指定した場合、応答データはJSONP(JavaScript Object Notation with Padding)を使用して形式設定され、JavaScript関数呼び出しでラップされます。

クライアントは、オプションで一意の要求識別子(*`reqId`*)を指定できます。この識別子は応答で返され、クライアントは非同期で受信した複数の応答を区別できます。 一般的な応答の一般的な構造は次のとおりです。

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

`s7jsonResponse` JavaScript関数は、クライアントによって定義される必要があります。 最も簡単な形式では、関数は次のようになります。

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

JSONP応答形式をサポートするリクエストでは、 `req=`パラメーターの拡張構文を使用して、JSコールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.

Dynamic Media Image Serving Viewersパッケージには、画像サービングからJSONP形式のデータを要求して解析するユーティリティが含まれています。

JSONP形式について詳しくは、 [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP)を参照してください。

JSON形式について詳しくは、 [www.json.org](https://www.json.org)を参照してください。

[req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)も参照してください。
