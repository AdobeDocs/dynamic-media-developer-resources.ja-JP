---
title: JSONP プロパティ
description: jsonpがレスポンス形式として指定されている場合、応答データは、JavaScript関数呼び出しでラップされたJSONP （パディング付きJavaScript Object Notation）を使用してフォーマットされます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
TQID: 'https://experienceleague.adobe.com/pMirwhZ5n0mVuK2If4kJz3XDQZPDhORJCZBLsDf2C8I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 212
ht-degree: 0%

---

# JSONP プロパティ{#jsonp-properties}

jsonpがレスポンス形式として指定されている場合、応答データは、JavaScript関数呼び出しでラップされたJSONP （パディング付きJavaScript Object Notation）を使用してフォーマットされます。

クライアントは、オプションの一意のリクエスト ID （*`reqId`*）を指定できます。この識別子は、応答で返され、クライアントが非同期で受信した複数の応答を区別できるようにします。 典型的な応答は、次の一般的な構造を持っています。

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

JSONP応答形式をサポートするリクエストでは、`req=` パラメーターの拡張構文を使用してJS コールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler]`

`<reqHandler>`構文は、JSONP応答に存在するJS ハンドラーの名前です。 a ～ z、A ～ Z、および0 ～ 9文字のみ使用できます。 オプション。 デフォルトは`s7jsonResponse`です。

Dynamic Media Image Serving Viewers パッケージには、Image ServingからJSONP形式のデータをリクエストおよび解析するユーティリティが含まれています。

JSONP形式について詳しくは、[https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP)を参照してください。

JSON形式について詳しくは、[www.json.org](https://www.json.org/json-en.html)を参照してください。

[req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)も参照してください。
