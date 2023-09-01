---
title: マップ
description: 画像マップデータ。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---

# マップ{#map}

画像マップデータ。

`req=map[,text|{xml[, *`エンコード`*]}|{json[&id= *`reqId`*]}]`

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

戻り値 `catalog::Map` 追加のコマンドを指定せずに単純なカタログエントリを照会する場合は変更を加えずに、 `catalog::maxPix`) をクリックします。

要求で他のコマンドが指定されている場合は、複合イメージマップが返されます。 合成画像マップは、すべての画像の拡大/縮小、切り抜き、回転、レイヤーを行うことによって生成されます `catalog::Map` および/または `map=` イメージデータがを使用する場合と同様に、リクエストに含まれるコマンド `req=img`.

指定 `text` または、2 番目のパラメーターを省略して、画像マップのデータを `HTML <AREA>` 応答 MIME タイプを持つ要素文字列 `text/plain`.

指定 `xml` したがって、応答を XML 形式ではなくHTMLできます。 オプションでテキストエンコーディングを指定できます。 デフォルトはです。 `UTF-8`.

空の文字列（または空）を返します `<AREA>` 要素 ) 指定したカタログオブジェクトのマップデータが見つからなかった場合、または `<AREA>` 画像を切り抜いた後も、要素は残ります。

HTTP 応答は、TTL に基づいてキャッシュ可能です。 `catalog::Expiration`.

JSONP 応答形式をサポートするリクエストでは、の拡張構文を使用して JS コールバックハンドラーの名前を指定できます。 `req=` パラメーター：

`req=...,json [&handler = reqHandler ]`

The `<reqHandler>` は、JSONP 応答に存在する JS ハンドラーの名前です。 a ～ z、A ～ Z、0 ～ 9 文字のみ使用できます。 オプション。デフォルトはです。 `s7jsonResponse`.

詳しくは、 [画像マップ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
