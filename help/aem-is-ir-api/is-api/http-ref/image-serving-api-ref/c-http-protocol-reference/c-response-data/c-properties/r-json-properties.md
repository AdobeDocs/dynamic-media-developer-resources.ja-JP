---
description: 応答形式としてjsonpを指定した場合、応答データはJSONP（パディング付きのJavaScript Object Notation）を使用して形式設定され、JavaScript関数の呼び出しでラップされます。
seo-description: 応答形式としてjsonpを指定した場合、応答データはJSONP（パディング付きのJavaScript Object Notation）を使用して形式設定され、JavaScript関数の呼び出しでラップされます。
seo-title: JSONPプロパティ
solution: Experience Manager
title: JSONPプロパティ
topic: Scene7 Image Serving - Image Rendering API
uuid: e53d75f2-9b43-4e8f-8191-66f69f344cdd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# JSONPプロパティ{#jsonp-properties}

応答形式としてjsonpを指定した場合、応答データはJSONP（パディング付きのJavaScript Object Notation）を使用して形式設定され、JavaScript関数の呼び出しでラップされます。

クライアントは、応答で返され、非同期に受信した複数の応答をクライアントが区別できるように、オプションの一意の要求識別子( *`reqId`*)を指定できます。 一般的な応答の一般的な構造は、次のとおりです。

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

JavaScript関数 `s7jsonResponse` は、クライアントが定義する必要があります。 最も単純な形式では、関数は次のようになります。

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

JSONP応答形式をサポートするリクエストを使用すると、次のパラメーターの拡張構文を使用してJSコールバックハンドラーの名前を指定で `req=` きます。

`req=...,json [&handler = reqHandler]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。 a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.

Scene7画像サービングビューアパッケージには、画像サービングからJSONP形式のデータを要求し、解析するユーティリティが含まれています。

JSONP形式につ [いて詳しくは](http://en.wikipedia.org/wiki/JSONP) 、http://en.wikipedia.org/wiki/JSONPを参照してください。

JSON形式につ [いて詳しくは](http://www.json.org) 、www.json.orgを参照してください。

「 [req」も参照](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)。
