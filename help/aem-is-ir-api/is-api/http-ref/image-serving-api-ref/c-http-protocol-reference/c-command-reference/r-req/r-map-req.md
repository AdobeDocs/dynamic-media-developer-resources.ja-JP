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
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 3%

---


# マップ{#map}

画像マップデータ。

`req=map[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> エンコード</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>一意の要求識別子。 </p></td> 
 </tr> 
</table>

追加のコマンドが指定されていない単純なカタログエントリをクエリする場合、変更せずに`catalog::Map`を返します（`catalog::maxPix`に拡大縮小されません）。

要求に他のコマンドが指定されている場合は、`req=img`と同様に、要求に含まれるすべての`catalog::Map`コマンドや`map=`コマンドを拡大・縮小、切り抜き、回転、レイヤー化することによって得られる合成画像マップが返されます。

`text`を指定するか、2番目のパラメーターを省略して、応答MIMEタイプ`text/plain`を持つ`HTML <AREA>`要素文字列の形式で画像マップデータを返します。

応答をHTMLではなくXMLにフォーマットするには、`xml`を指定します。 テキストのエンコーディングはオプションで指定できます。 デフォルトは`UTF-8`です。

指定したカタログオブジェクトのマップデータが見つからない場合は空の文字列（または空の`<AREA>`要素）を返します。画像を切り抜いた後に`<AREA>`要素が残らない場合も同様です。

HTTP応答は、`catalog::Expiration`に基づいてTTLでキャッシュ可能です。

JSONP応答形式をサポートするリクエストでは、`req=`パラメーターの拡張構文を使用して、JSコールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.

[画像マップ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)を参照してください。
