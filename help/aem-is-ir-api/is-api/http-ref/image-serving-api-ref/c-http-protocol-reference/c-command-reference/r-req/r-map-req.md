---
description: 画像マップデータ。
seo-description: 画像マップデータ。
seo-title: マップ
solution: Experience Manager
title: マップ
topic: Scene7 Image Serving - Image Rendering API
uuid: 57cb0fcf-5a07-4109-bfd4-ef9aaf794b27
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# マップ{#map}

画像マップデータ。

`req=map[,text|{xml[, *`encodingreqId`*]}|{json[&id= *``*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> エンコード</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>一意の要求識別子。 </p></td> 
 </tr> 
</table>

追加のコ `catalog::Map` マンドが指定されていない単純なカタログエントリをクエリする場合、変更なしで返されます(拡大・縮小は行わ `catalog::maxPix`れません)。

要求で他のコマンドが指定されている場合は、画像データと同様に、要求に含まれるすべてのコマンドやコマンドを拡大・縮小、切り抜き、回転、レイヤー化することで得られる、合成画像マ `catalog::Map` ップが返されます `map=``req=img`。

応答MIME `text` タイプを持つ要素文字列の形式で画像マップデータを返す場合は、2番目のパラメ `HTML <AREA>` ーターを指定または省略しま `text/plain`す。

応答をHTML `xml` ではなくXMLとして形式設定する場合に指定します。 オプションでテキストのエンコーディングを指定できます。 The default is `UTF-8`.

指定したカタログオブジェクトのマップデータが見つからな `<AREA>` い場合、または画像を切り抜いた後に要素が残らない場合は、空の文字列( `<AREA>` または空の要素)を返します。

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

JSONP応答形式をサポートするリクエストを使用すると、次のパラメーターの拡張構文を使用してJSコールバックハンドラーの名前を指定で `req=` きます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。 a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.

See [Image Maps](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
