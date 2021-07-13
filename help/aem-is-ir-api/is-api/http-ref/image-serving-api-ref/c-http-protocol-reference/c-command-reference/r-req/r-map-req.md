---
description: 画像マップデータ。
solution: Experience Manager
title: マップ
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 2%

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
  <td class="stentry"> <p>一意のリクエスト識別子。 </p></td> 
 </tr> 
</table>

追加のコマンドを指定せずに、単純なカタログエントリをクエリする場合、`catalog::Map`を変更せずに返します（`catalog::maxPix`に拡大/縮小されません）。

リクエストで他のコマンドが指定されている場合、合成画像マップが返されます。このマップは、画像データが`req=img`と一緒にあるように、リクエストに含まれるすべての`catalog::Map`および`map=`コマンドの拡大/縮小、切り抜き、回転、および重ね合わせによって得られます。

`text`を指定するか、2番目のパラメーターを省略して、応答MIMEタイプ`text/plain`を持つ`HTML <AREA>`要素文字列の形式で画像マップデータを返します。

`xml`を指定して、応答をHTMLではなくXMLで書式設定します。 オプションで、テキストエンコーディングを指定できます。 デフォルトは`UTF-8`です。

指定したカタログオブジェクトのマップデータが見つからない場合や、画像を切り抜いた後に`<AREA>`要素が残らない場合は、空の文字列（または空の`<AREA>`要素）を返します。

HTTP応答は、`catalog::Expiration`に基づいてTTLでキャッシュ可能です。

JSONP応答形式をサポートするリクエストでは、 `req=`パラメーターの拡張構文を使用して、JSコールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.

[画像マップ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)を参照してください。
