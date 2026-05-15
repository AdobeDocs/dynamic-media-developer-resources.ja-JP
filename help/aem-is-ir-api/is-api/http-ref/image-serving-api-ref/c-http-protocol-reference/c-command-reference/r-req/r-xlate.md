---
description: 使用可能なロケール固有のバージョン。 リクエストパスで指定されたカタログ IDの使用可能なロケール固有のバージョンのリストを返します。
solution: Experience Manager
title: xlate
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bf5b3cb7-9792-4eca-a1aa-55aa4089b4d4
TQID: 'https://experienceleague.adobe.com/Ac-h7oQm6fF01YUOz2RQ25dyqLj02shurvkxulWJUHk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 115
ht-degree: 2%

---

# xlate{#xlate}

使用可能なロケール固有のバージョン。 リクエストパスで指定されたカタログ IDの使用可能なロケール固有のバージョンのリストを返します。

`req=xlate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8970A3A5A64F4DC2B184E251993390C5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>一意のリクエスト ID。 </p></td> 
 </tr> 
</table>

[ オブジェクト Idの翻訳](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414)を参照してください。

以下に例を挙げます。

`xlate.translatedIds=image,image_fr,image_de`

HTTP応答は、`catalog::Expiration`に基づくTTLでキャッシュできます。

JSONP応答形式をサポートするリクエストでは、`req=` パラメーターの拡張構文を使用してJS コールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`は、JSONP応答に存在するJS ハンドラーの名前です。 a ～ z、A ～ Z、および0 ～ 9文字のみ使用できます。 オプション。 デフォルトは`s7jsonResponse`です。
