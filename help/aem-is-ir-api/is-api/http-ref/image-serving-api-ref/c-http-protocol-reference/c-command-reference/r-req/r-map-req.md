---
title: マップ
description: 画像マップデータ。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# マップ{#map}

画像マップデータ。

`req=map[,text|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> エンコーディング </span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>一意のリクエスト識別子。 </p></td> 
 </tr> 
</table>

追加のコマンドが指定されていない単純なカタログエントリに対してクエリを実行する場合、`catalog::Map` を変更せずに返します（`catalog::maxPix` に合わせて拡大縮小されません）。

リクエストで他のコマンドが指定されている場合は、合成画像マップが返されます。 合成画像マップは、画像データが `catalog::Map` で行われるのと同様に、リクエストに含まれるすべての `map=` および/または `req=img` コマンドの拡大縮小、切り抜き、回転、レイヤー化によって派生されます。

2 番目のパラメーター `text` 指定するか省略すると、応答 MIME タイプ `HTML <AREA>` を持つ `text/plain` 要素文字列の形式で画像マップデータを返すことができます。

HTMLの代わりに XML として応答をフォーマットできるように、`xml` を指定します。 テキストエンコーディングは、オプションで指定できます。 デフォルトは `UTF-8` です。

指定したカタログオブジェクトのマップデータが見つからなかった場合、または画像を切り抜いた後も `<AREA>` 要素が残っていない場合は、空の文字列（または空の `<AREA>` 要素）を返します。

HTTP 応答は、`catalog::Expiration` に基づく TTL でキャッシュ可能です。

JSONP 応答形式をサポートするリクエストでは、パラメーターの拡張構文を使用して JS コールバックハンドラーの名前 `req=` 指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP 応答に存在する JS ハンドラーの名前です。 a ～ z、A ～ Z、0 ～ 9 文字のみを使用できます。 オプション。 デフォルトは `s7jsonResponse` です。

[&#x200B; 画像マップ &#x200B;](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab) を参照してください。
