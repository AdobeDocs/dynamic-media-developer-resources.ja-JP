---
title: マップ
description: 画像マップデータ：
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
TQID: 'https://experienceleague.adobe.com/Ly1JWjeEyZWUEiyVcv-t-OKf0cp6uuMsbR0B6BE1fhY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 224
ht-degree: 1%

---

# マップ{#map}

画像マップデータ：

`req=map[,text|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> エンコーディング </span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>一意のリクエスト ID。 </p></td> 
 </tr> 
</table>

追加のコマンドを指定せずに単純なカタログエントリをクエリする場合は、変更なしで`catalog::Map`を返します（`catalog::maxPix`に拡張しません）。

リクエストで他のコマンドが指定されている場合は、合成画像マップが返されます。 合成画像マップは、画像データが`req=img`と同じように、リクエストに含まれるすべての`catalog::Map`および/または`map=` コマンドをスケーリング、トリミング、回転、レイヤー化することによって得られます。

`text`を指定するか、2番目のパラメーターを省略して、応答MIME タイプ `text/plain`の`HTML <AREA>`要素文字列の形式で画像マップデータを返せます。

`xml`を指定して、HTMLの代わりにXMLとして応答をフォーマットできるようにします。 テキストエンコーディングはオプションで指定できます。 デフォルトは`UTF-8`です。

指定されたカタログオブジェクトにマップデータが見つからなかった場合、または画像の切り抜き後に`<AREA>`要素が残っていない場合に、空の文字列（または空の`<AREA>`要素）を返します。

HTTP応答は、`catalog::Expiration`に基づくTTLでキャッシュできます。

JSONP応答形式をサポートするリクエストでは、`req=` パラメーターの拡張構文を使用してJS コールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`は、JSONP応答に存在するJS ハンドラーの名前です。 a ～ z、A ～ Z、および0 ～ 9文字のみ使用できます。 オプション。 デフォルトは`s7jsonResponse`です。

[画像マップ ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)を参照してください。
