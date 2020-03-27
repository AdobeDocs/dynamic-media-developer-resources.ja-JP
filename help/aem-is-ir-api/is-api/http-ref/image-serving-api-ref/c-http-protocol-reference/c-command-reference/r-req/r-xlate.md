---
description: ロケール固有の使用可能なバージョン。 要求パスで指定されたカタログIDの使用可能なロケール固有のバージョンのリストを返します。
seo-description: ロケール固有の使用可能なバージョン。 要求パスで指定されたカタログIDの使用可能なロケール固有のバージョンのリストを返します。
seo-title: xlate
solution: Experience Manager
title: xlate
topic: Scene7 Image Serving - Image Rendering API
uuid: 4c2370e5-1d46-4242-89bb-a5ce416ef63c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# xlate{#xlate}

ロケール固有の使用可能なバージョン。 要求パスで指定されたカタログIDの使用可能なロケール固有のバージョンのリストを返します。

`req=xlate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8970A3A5A64F4DC2B184E251993390C5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>一意の要求識別子。 </p></td> 
 </tr> 
</table>

詳しくは、オ [ブジェクトIDの変換を参照してくださ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414)い。

例：

`xlate.translatedIds=image,image_fr,image_de`

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

JSONP応答形式をサポートするリクエストを使用すると、次のパラメーターの拡張構文を使用してJSコールバックハンドラーの名前を指定で `req=` きます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。 a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.
