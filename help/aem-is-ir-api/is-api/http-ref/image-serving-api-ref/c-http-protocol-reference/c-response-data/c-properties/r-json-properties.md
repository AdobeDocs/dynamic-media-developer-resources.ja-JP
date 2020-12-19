---
description: 応答形式としてjsonpを指定した場合、応答データはJSONP（パディング付きのJavaScriptオブジェクト表記）を使用して形式設定され、JavaScript関数の呼び出しでラップされます。
seo-description: 応答形式としてjsonpを指定した場合、応答データはJSONP（パディング付きのJavaScriptオブジェクト表記）を使用して形式設定され、JavaScript関数の呼び出しでラップされます。
seo-title: JSONPプロパティ
solution: Experience Manager
title: JSONPプロパティ
topic: Scene7 Image Serving - Image Rendering API
uuid: e53d75f2-9b43-4e8f-8191-66f69f344cdd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 1%

---


# JSONPプロパティ{#jsonp-properties}

応答形式としてjsonpを指定した場合、応答データはJSONP（パディング付きのJavaScriptオブジェクト表記）を使用して形式設定され、JavaScript関数の呼び出しでラップされます。

クライアントは、オプションで一意の要求識別子(*`reqId`*)を指定できます。これは応答で返され、クライアントは非同期に受信した複数の応答を区別できます。 一般的な応答の一般的な構造は次のとおりです。

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

`s7jsonResponse` JavaScript関数は、クライアントが定義する必要があります。 最も単純な形式では、関数は次のようになります。

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

JSONP応答形式をサポートするリクエストでは、`req=`パラメーターの拡張構文を使用して、JSコールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.

Scene7画像サービングビューアパッケージには、画像サービングからJSONP形式のデータを要求し、解析するユーティリティが含まれています。

JSONP形式について詳しくは、[http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP)を参照してください。

JSON形式について詳しくは、[www.json.org](http://www.json.org)を参照してください。

[req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)も参照してください。
