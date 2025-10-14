---
description: 使用可能なロケール固有のバージョン。 リクエストパスで指定されたカタログ ID の使用可能なロケール固有のバージョンのリストを返します。
solution: Experience Manager
title: xlate
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bf5b3cb7-9792-4eca-a1aa-55aa4089b4d4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 1%

---

# xlate{#xlate}

使用可能なロケール固有のバージョン。 リクエストパスで指定されたカタログ ID の使用可能なロケール固有のバージョンのリストを返します。

`req=xlate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8970A3A5A64F4DC2B184E251993390C5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>一意のリクエスト識別子。 </p></td> 
 </tr> 
</table>

[&#x200B; オブジェクト Id 変換 &#x200B;](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414) を参照してください。

以下に例を挙げます。

`xlate.translatedIds=image,image_fr,image_de`

HTTP 応答は、`catalog::Expiration` に基づく TTL でキャッシュ可能です。

JSONP 応答形式をサポートするリクエストでは、パラメーターの拡張構文を使用して JS コールバックハンドラーの名前 `req=` 指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP 応答に存在する JS ハンドラーの名前です。 a ～ z、A ～ Z、0 ～ 9 文字のみを使用できます。 オプション。 デフォルトは `s7jsonResponse` です。
